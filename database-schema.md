# E-commerce Database Schema

## Users Table
- UserId (PK)
- Name
- Email
- PasswordHash
- Phone
- CreatedAt

## Sellers Table
- SellerId (PK)
- Name
- Email
- Phone
- CreatedAt

## Products Table
- ProductId (PK)
- Name
- Description
- Price
- StockQuantity
- CategoryId (FK)
- SellerId (FK)
- ImageUrl
- CreatedAt

## Categories Table
- CategoryId (PK)
- CategoryName

## Cart Table
- CartId (PK)
- UserId (FK)

## CartItems Table
- CartItemId (PK)
- CartId (FK)
- ProductId (FK)
- Quantity

## Orders Table
- OrderId (PK)
- UserId (FK)
- TotalAmount
- OrderDate
- Status

## OrderItems Table
- OrderItemId (PK)
- OrderId (FK)
- ProductId (FK)
- Quantity
- Price

## Payments Table
- PaymentId (PK)
- OrderId (FK)
- PaymentMethod
- PaymentStatus
- PaymentDate

## Addresses Table
- AddressId (PK)
- UserId (FK)
- AddressLine
- City
- State
- Pincode

## Shipments Table
- ShipmentId (PK)
- OrderId (FK)
- AddressId (FK)
- CourierName
- TrackingNumber
- ShipmentStatus
- ShippedDate
- DeliveredDate

## DeliveryStatusHistory Table
- StatusId (PK)
- ShipmentId (FK)
- Status
- UpdatedAt

## Reviews Table
- ReviewId (PK)
- UserId (FK)
- ProductId (FK)
- Rating
- Comment
