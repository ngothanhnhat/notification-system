# Notification System
Created by: Ngo Thanh Nhat
## Diagram
![Screenshot from 2023-10-23 21-48-19](https://github.com/ngothanhnhat/notification-system/assets/9256201/548076e2-c8c0-493c-b22d-74234ddceaee)
## Explanation
### API
We need some APIs to interact with notification system:
- create topic
- publish
- subscribe
### Load Balancer
Used to increase capacity (concurrent users) and reliability of applications
### Notification Service
It is a lightweight web service, it handles all request and put them to the Queue
### Prepare Worker
It is a web service, that contains actions:
- Request validation
- Authentication/Authorization
- Caching
- Request Duplication
- Request Dispatching
- Priority Service
### Metadata Service
A lightweight web service, it provides some functions to interact with persistent storage.
### Delivery Worker
A service to handle events from the Queue, it needs more information from Notification Adapter.
### Notification Adapters
We can implement some adapters like:
- SMS Adapter
- Email Adapter
- In-App Adapter
