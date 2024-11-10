## all-in-one-docker-bigdataops

**all-in-one-docker-bigdataops** is a comprehensive Docker Compose environment that simplifies Big Data operations by bundling Hadoop, Spark, Hive, Hue, and Airflow into a ready-to-run stack, with example workflows, quick setup, and easy customization, making it ideal for learning, development, and testing in Big DataOps.

### Key Features:
- **Fully Integrated Big Data Tools**: Pre-configured and ready to use, including Hadoop for distributed storage and processing, Spark for big data analytics, Hive for SQL-based querying, Hue for a web-based UI, and Airflow for orchestrating complex data pipelines.
- **Quick Setup**: Get started with a single `make start-all` command. No more dealing with tedious configurations or dependency issues.
- **Versatile Usage**: Ideal for learning, development, testing, and small-scale production environments.
- **Example Workflows**: Includes sample jobs and scripts to demonstrate the capabilities of the stack, helping you kickstart your big data projects.
- **Customizable**: Easily extend or modify the stack to fit your specific use cases.

### Why Use This Repository?
- **Ease of Use**: Simplifies the setup process, so you can focus on developing and testing your big data solutions.
- **All-in-One Solution**: No need to piece together different tools. Everything is bundled in a single, cohesive package.
- **Community-Driven**: Designed to be accessible, well-documented, and easy to discover, with the goal of becoming a go-to resource for Big DataOps on Docker.

### How to use?
- Ensure you have docker installed + make 
- You can find useful commands in Makefile
- When using airflow, remember to add the following connections:
  - conn_id 'spark_docker' --conn-type spark --conn-host spark://spark-master --conn-port 7077
  - conn_id 'ssh_hadoop' --conn-type ssh --conn-host namenode --conn-port 22 --conn-login root --conn-password root123
- In case you want to deploy the full infrastructure, just:
```
make start-all
```
