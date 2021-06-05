# Field Service - Order Management. Domain Model[^1]

- [Field Service - Order Management. Domain Model[^1]](#field-service---order-management-domain-model1)
  - [Introduction](#introduction)
  - [Customer Order (Business Object)](#customer-order-business-object)
  - [Fileld Service Management (Grouping)](#fileld-service-management-grouping)
    - [Work Order (Business Object)](#work-order-business-object)
    - [Work (Business Object)](#work-business-object)
  - [Service Order Management (Grouping)](#service-order-management-grouping)
    - [Customer Facing Service Order (Business Object)](#customer-facing-service-order-business-object)
    - [Resource Facing Service Order (Business Object)](#resource-facing-service-order-business-object)
    - [Field Service RFS Order (Business Object)](#field-service-rfs-order-business-object)

## Introduction
![Field Service - Order Management. Domain Model][embedView]

## Customer Order (Business Object)

**Relationships**
|From|Relationship|To|Name|Description|
|---|---|---|---|---|
|Customer Order|Composition Relationship|[Customer Facing Service Order (Business Object)](#customer-facing-service-order-business-object)|[1..*]||

## Fileld Service Management (Grouping)

**Relationships**
|From|Relationship|To|Name|Description|
|---|---|---|---|---|
|Fileld Service Management|Composition Relationship|[Work Order (Business Object)](#work-order-business-object)|||
|Fileld Service Management|Composition Relationship|[Work (Business Object)](#work-business-object)|||

### Work Order (Business Object)

**Relationships**
|From|Relationship|To|Name|Description|
|---|---|---|---|---|
|Work Order|Composition Relationship|[Work (Business Object)](#work-business-object)|[1..*]||

### Work (Business Object)

## Service Order Management (Grouping)

**Relationships**
|From|Relationship|To|Name|Description|
|---|---|---|---|---|
|Service Order Management|Composition Relationship|[Customer Facing Service Order (Business Object)](#customer-facing-service-order-business-object)|||
|Service Order Management|Composition Relationship|[Resource Facing Service Order (Business Object)](#resource-facing-service-order-business-object)|||
|Service Order Management|Composition Relationship|[Field Service RFS Order (Business Object)](#field-service-rfs-order-business-object)|||

### Customer Facing Service Order (Business Object)

**Relationships**
|From|Relationship|To|Name|Description|
|---|---|---|---|---|
|Customer Facing Service Order|Aggregation Relationship|[Resource Facing Service Order (Business Object)](#resource-facing-service-order-business-object)|[1..*]||

### Resource Facing Service Order (Business Object)

### Field Service RFS Order (Business Object)

**Relationships**
|From|Relationship|To|Name|Description|
|---|---|---|---|---|
|Field Service RFS Order|Specialization Relationship|[Resource Facing Service Order (Business Object)](#resource-facing-service-order-business-object)|||
|Field Service RFS Order|Association Relationship|[Work (Business Object)](#work-business-object)|||

[embedView]: dm.png
[^1]: Generated: Thu Jun 03 2021 00:19:28 GMT+0800 (SGT)
