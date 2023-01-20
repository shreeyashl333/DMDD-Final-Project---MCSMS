# DAMG 6210 Database Management and Database Design -Final-Project---MCSMS
Associated with coursework as a graduate student at Northeastern University, Boston, MA

# Massachusetts Courier Service Management System

# Background
    It is currently very vital for people to ship or receive commodities such as imported furniture,
    electrical equipment, gifts, commercial goods, and so on. However, the sending and receiving
    process is not particularly user-friendly. But, there lies a major inconvenience of constantly being
    in touch with the courier office for updates about the shipments. Courier offices have to
    communicate with multiple people in order to receive updates and send them to the customers.
    Hence, a management system would be of paramount importance in this situation.
    The Massachusetts Courier Service Management System is a system that enables customers to
    order courier services to send goods from a source location to a specified destination. Employees
    can use this system to track the progress of the couriers as they deliver packages.
    
# Mission Statement/ Objectives
    ● To develop a centralized system to keep track of all the information regarding courier
      orders and their movement from the point of origin to the point of destination, which can
      be accessed by customers to track their orders up until delivery and staff to use the
      system to effectively coordinate the delivery of the items.
    ● To track activities such as booking, delivery, status checks and provide timely notification
      updates to customers.
    ● To provide effective time management, which ensures that remote labor operates well
      while accommodating various locations.
    ● To offer priority based and location specific services, with varied payment options.
    ● To increase the cost effectiveness as the unwanted labor services can be easily replaced
      by the database system.
    ● To improve team collaboration on multiple levels for proper handling of the product and
      ensure on-time product delivery.
      
# Discussed Business Problem :
    1. Developing a system that enables tracking and courier management.
    2. Providing different modes of delivery so that even during the peak COVID times,
    hassle free and contactless delivery would be possible.
    3. Providing priority based services so that customizing and delivery of packages
    becomes a lot easier.
    4. Create a centralized system that can be accessed by customers to track their orders
    through delivery and staff to use the system to efficiently coordinate the delivery of
    the items.
    5. The system should keep track of all the information regarding courier orders and their
    movement from the point of origin to the point of destination.
    6. Enhance multi-level teamwork to ensure timely delivery of the product and proper
    management of the product.
# Entities :
    1. Customers
    2. Package
    3. Address
    4. Payments
    5. Shipment
    6. Offices
    7. Warehouse
    8. Employee
    9. Role
    10. Vehicle
    11. Package_Type
    12. Delivery_Mode
    13. Priority_Type
    14. Service_Location
    15. Package
    16. Priority
    17. Delivery_Mode
    18. Service_Location
# Relationships between entities:
    1. Any number of packages may be ordered by the customer for delivery via courier. A
        customer must pay only after placing an order for a package (Payments being the
        associative entity between Customer and Package).
    2. Each Package must have one Priority, and the same Priority can be assigned to
      multiple Packages. Also each package must have one Delivery Mode assigned to it.
    3. An Office may contain 0 or many Packages. One Package must be associated with
      one Office only.
    4. Offices must have one Warehouse only and vice-versa.
    5. One Package can be a part of One Shipment, and One Shipment can have many
      Packages.
    6. One Warehouse can ship multiple Shipments. Any number of shipments can be
       received by one Warehouse.
    7. One shipment must be carried in one Vehicle to the nearest Warehouse and vehicle
      may have any number of shipments.
    8. Delivery person will carry the package from the nearest Warehouse to the receiver’s
      address.a
    9. An employee may be assigned to 0 or one vehicle . A vehicle can only have one
      Employee that drives it.
    10. Each Employee can have one role, and one Role can have many Employees.
    11. An office must have 1 or many employees, and an employee may work only in one
      office.
    12. A warehouse must have 1 or many employees, and an employee may work only in
      one warehouse.
    13. One service location can have many Packages. Each Package must be in one
      service location.
# Key Design Decisons:
    1. Customers are able to send multiple packages to any serviceable location.
    2. Each Package must be associated with a Payment which the Customer makes.
    3. The priority and delivery mode must and delivery mode for each package must be
      assigned.
    4. The Package consists of the Current_Location and Delivery_Status attributes which
      helps in tracking the location of the courier to the customer.
    5. Each Office will have one warehouse from which shipment will be dispatched to the
      nearest destination Warehouse.
    6. There will be a manager and staff members assigned to each office.
    7. The loading and unloading of shipments will be handled by staff in each warehouse.
    8. Each shipment will be transported by a vehicle that the warehouse manager will
      designate to the employees whose primary duty is driving.
    9. A driver (an Employee) will be appointed to each vehicle to transport the shipments
      between the Warehouses.
    10. The shipment will finally be delivered to the receiver by the delivery person from the
      final warehouse.
      
      ![ER-MCSMv1](https://user-images.githubusercontent.com/114704336/213800233-5f7fdfe5-0172-4401-b2c8-42e5053eb28d.png)
