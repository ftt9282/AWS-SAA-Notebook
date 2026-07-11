This is different than a traditional [[Aurora]] DB setup. There is no capacity planning needed, and instantiation and auto-scaling is done based on actual usage. You pay per second, and it can be more cost-effective if there are infrequent or intermittent workloads.

The "serverless" setup on the backend is a proxy fleet that is managed by Aurora that scales as needed.