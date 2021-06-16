# hydrosim
Repository for information related to the Hydrosim project.

## Compute Requirements

### Web Server

Server to host the node.js API that will make the data available to the front end & for direct download of the simulation results. 

Requirements

- Large storage capacity (>10GB)
- The ability to read from NetCDF files and return JSON files
- Multiple cores to handle API requests in parrallel
- Limited computation requirements

### Compute Server

Server to run the hydrodynamic simulations and then transfer the results to the web server

Requirements

- Large RAM, high performance CPU
- Ability to run computationally intensive simulations in parrallel
- Limited storage requirements (< 100GB)

## Hardware Options

### Eawag

Option 1 is to purchase the two machines and have the Eaway IT department run and maintain them.

Pros:
- Full access to the machines
- Unlimited customisation
- No monthly costs
- Storage is very cheap
- Easy to align with existing procurement proceedures and include in project budget
Cons:
- Large upfront cost (>$10K)
- Maintenance and repairs limited to office hours
- Limited scalability (if server spec is wrong little option to make changes)
- Catastrophic hardware issues could stop the project
- Long setup time (define server specs, procurement, etc.)
- Eawag is responsible for the backups
- Dependant on the Eawag network, any Eawag outages will effect the performance of the API

### Cloud Provider (e.g. AWS)

Option 2 is to use pay by use servers from a cloud provider such as AWS.

Pros:
- Rapid deployment (< 1hr)
- Scalability (fast and easy to increase compute power/ storage)
- Option to spawn multiple low power servers rather than running simulations in parrallel
- No upfront cost
- Many services in one place (database, frontend (AWS amplify), S3 etc.)
- 24hr service and maintenace
Cons:
- Monthly costs can grow rapidly (hard to align with project budget)

### Dedicated Cloud Server (e.g. OVHcloud)

Option 3 is to purchase dedicated cloud servers.

Pros:
- Quick deployment (< 24hrs)
- No upfront cost
- Many services in one place (database, frontend (AWS amplify), S3 etc.)
- 24hr service and maintenace
- Monthly cost is predictable and lower than for virtual machines
Cons:
- Difficult to scale
- Costly to have multiple servers
- May not be possible to get the exact server specs you want
