# Load Balancing OutSystems Applications

**Important: **This guide applies only to on-premises/private cloud installations. It does not apply to OutSystems Enterprise Cloud, where the load balancing mechanism is provided to the customer by OutSystems (where applicable).

[OutSystems Platform scales horizontally with the addition of front-ends to suit the needed capacity. ](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Designing_OutSystems_Infrastructures/03_Scaling_and_high_availability_for_OutSystems_Platform_servers)In a farm environment, balancing the application load across multiple front-ends is a basic requirement to ensure higher availability.

OutSystems Platform does not include a load balancing mechanism of its own. To balance load between front-ends in an OutSystems Platform farm, you must resort to one of many load balancing mechanisms on the market. 
