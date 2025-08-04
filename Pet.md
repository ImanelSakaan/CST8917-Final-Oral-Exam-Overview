```mermaid
graph TB
    subgraph Traditional
        A1[Order Service Container]
        B1[Notification Microservice]
        C1[Manual Image Upload]
        D1[Cron Job on VM]
    end

    subgraph Serverless
        A2[Order Processing Function <br> (Service Bus Trigger)]
        B2[Notification Function <br> (Queue Trigger)]
        C2[Image Optimization Function <br> (Blob Trigger)]
        D2[Inventory Report Function <br> (Timer Trigger)]
    end

    A1 --> A2
    B1 --> B2
    C1 --> C2
    D1 --> D2
end
```    
