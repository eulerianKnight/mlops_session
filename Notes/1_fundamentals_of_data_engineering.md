# Fundamental of Data Engineering

## What is Data Engineering?

**Think about it...As per you, what data engineers do?**

- "Data Engineering is the development, implementation, and maintenance of systems and processes that take in raw data and produce high-quality, consistent information that supports downstream use cases, such as analysis and machine learning. Data engineering is the intersection of security, data management, DataOps, data architecture, orchestration, and software engineering."
- "Get data from sources, do something useful to it, serve it."
- Data Engineering lifecycle:

![img.png](../files/data_engineering/img.png)

- *What is unlikely to change in 5–10 years?*

### Brief History of Data Engineering

- Database Management Systems.
  - Timeframe: 1960s and 1970s
  - Various types of databases.
  - Relational database and data model: Ted Codd at IBM
  - Ways to interface with databases: SQL.
- Data Warehouse
  - Timeframe: 1980s and 1990s
  - Transactional -> Analytics
  - Data warehouse architecture: Bill Inmon
  - Dimensional data model: Ralph Kimball
  - Analytics and Business Intelligence (BI)
- Business Intelligence and Analytics
  - Timeframe: 1990s and 2000s.
  - The internet and the Worldwide web.
  - Broadband internet connections.
  - 'Web Scale Data'
  - New Approaches: Hadoop, NoSQL databases, etc.
  - Big Data: 3 V's. Volume, Velocity and Variety.
- Data Science
  - Timeframe: 2000s to mid 2010s
  - New tools and techniques for handling data, big and small
  - Machine Learning became popular.
  - Data Science involves ML, predictive and prescriptive analytics and more.
- Rise of Data Engineering
  - Timeframe: mid 2010s to present
  - Data Scientists spend a lot of time on non-data science work.
  - Machine Learning and Analytics goes mainstream.
  - Big Data tools become more accessible and easy to use.
  - How to provide a foundation for data science and analytics? *Data Engineering*
- Data Engineering today
  - Tools and practices are much simpler than the *Big Data* era.
  - Data Engineering is a hot and growing career field.
  - Abstraction = Data Engineers move up the value chain.
  - Data Engineering = Lifecycle Management.
- A Data Engineer:
  - Designs, builds and maintain data infrastructure.
  - Manages the data engineering lifecycle.
  - Ensure that data is available, reliable and ready for use in analytics, ML/AI and other data use cases.
- Tasks:
  - Designing and building data pipelines to collect data from various sources.
  - Building and managing data warehouses and data lakes.
  - Cleaning, modeling, and transforming data to make it consistent and usable.
  - Developing datasets for data analysis and data science.
  - Writing and managing data orchestration workflows.
- A Data Engineer manages the following aspects of the data engineering lifecycle:
  - Data creation in source systems.
  - Ingestion.
  - Storage.
  - Transformation.
  - Serving.

### Upstream and Downstream Stakeholders.

![img_1.png](../files/data_engineering/img_1.png)

1. **Software Engineer & Data Engineer**
    - A Software engineer typically
      - Sits upstream from a data engineer.
      - Designs, develops and tests software systems and applications.
      - Maintains the source systems that data engineers depend on.

2. **Data Engineer & Data Scientist**
   - A Data Scientist typically
     - Often sits downstream from a data engineer.
     - Uses data to solve business problems.
     - Rely on the systems and data provided by data engineers.

## Data Engineering Lifecycle

- Data Engineering lifecycle is a subset of Data lifecycle.
- Data lifecycle encompasses data across entire lifecycle, data engineering lifecycle focuses on stages that data engineers controls.
- Data Lifecycle Components:
  - Creation
  - Capture
  - Preparation
  - Usage
  - Archival
  - Deletion

### Stages of Data Engineering Lifecycle

#### 1. Data Generation from Source Systems.

- Every digital process generates data.
- Examples: databases, application servers, raw files, APIs, IOT devices, social media and ecommerce platforms, cars, and many more.
- Raw data from source systems is often complex and messy.

#### 2. Data Ingestion.

- Extract data from various source systems, move it, and prepare it for further use or storage.
- Batch or real-time ingestion.
- Might involve cleaning and data validation steps.
- From here, data can be stored, transformed, and served.

#### 3. Data Storage.

- Saving data in an organized and easy-to-understand manner that allows for easy retrieval.
- Several ways to store data: Relational database, File System, Blob storage, NoSQL database, Data Warehouse or data lake, and many more.
- Goal: Ensure data is easily accessible, secure, and organized.

#### 4. Data Transformation

- Data mutates and evolves into something different.
- Integrate other data sources.
- Convert to a state useful for analysis, machine learning and other downstream use cases.

#### 5. Serving Data

- Serve data to users and applications in a format ready for consumptions and use.
- Examples: Analysis, Predictive Modeling, Machine Learning, reverse ETL, data-powered applications, and more.

## The Undercurrents of Data Engineering

- The undercurrents are the glue that holds the data engineering lifecycle together.

![img_2.png](../files/data_engineering/img_2.png)

#### 1. Security

- Security must be a top priority throughout the data engineeringlifecycle.
- Security starts with YOU.
- Principle of the least privilege.
- Consider how security fits into how you handle data.
- Example: Encryption at rest and in transit, role-based access control (RBAC), tenancy.

#### 2. Data Management

- DAMA Body of Knowledge: Data Management is the development, execution, and supervision of plans, policies, programs, and practices that deliver, control, protect, and enhance the value of data and information assets throughout their lifecycle.
- Key areas important for data engineers:
  - Data Governance
  - Data Modeling and Design
  - Data Lineage
  - Storage and Optimization
  - Data Integration and Interoperability.
  - Data Lifecycle Management.
  - Ethics and Privacy.

#### 3. DataOps

- Key components: Automation, Observability and monitoring, Incident Response.

#### 4. Data Architecture


#### 5. Orchestration

- Key components:
  - Time or event-based
  - Efficient Task Management
  - Automated Error Handling
  - Scalability
  - Monitoring and Alerting
  - Directed Acyclic Graph (DAG)
- DAG
  - Graphs, Vertices and Edges.
  - Represents a series of activities.
  - No cycles or looping back on itself.
  - Driven by time or an event.
- Orchestration is not just a nice to have. It is key to making data engineering work.

#### 6. Software Engineering

- Software Engineering is the application of engineering principles to the design, development, testing and maintenance of software. It is a systematic approach to software development that aims to create high-quality, reliable and maintainable software.
- Many 'data' systems are software systems.
- Not just about 'coding Python or Java'
- General purpose of problem-solving.
- A Data Engineer should be able to write clean, readable and performant software.
- Test and debug code and systems.
- Design, Develop and maintain software.


## Data Architecture

- DMBOK describes: "Identifying the data needs of the eneterprise and designing and maintaining the master blueprints to meet those needs. Using master blueprints to guide data integration, control data assets, and align data investments with business strategy."
- TOGAF describes: "A description of the structure and interaction of the enterprise's major types and sources of data, logical data assets, physical data assets, and management resources."
- Joe Reis & Matt Housley: "Data Architecture is the design of systems to support the evolving data needs of an enterprise, achieved by flexible and reversible decisions reached through a careful evaluation of trade-offs."
- The Data Architecture is NOT:
  - The Data itself.
  - The tools and technology you use.
  - A one-time project.
  - Static.
- Major Architecture Concepts:
  - Domains and Services
  - Distributed systems, Scalability, and Designing for failure.
  - Tight vs Loose Coupling.
  - Greenfield vs Brownfield Architecture.

### Domains and Services:
- Domain: A Sphere of Knowledge, influence or activity. The subject area to which the user applies a program is the domain of the software.
- When architecting, it's critical to know what we are designing.
- Services: A Set of functionality whose goal is to accomplish a task.
- Example: Sales and Accounting Domains.

![img_3.png](../files/data_engineering/img_3.png)

### Distributed Systems, Scalability and Designing for Failure.

- Everything eventually fails.
- Distributed system: More than one point of failure, with built-in redundancy.
- Scalability: Increase system capacity.
- Elasticity: Automatically scale up and down based on workload.
- Availability: The percent of time a system is in an operational state.
- Reliability: The probability of a system meeting defined standards for its intended purpose.

### Tight vs Loose Coupling

- Tight Coupling: High Interdependence between systems.
- Loose Coupling: Systems are largely independent.
- Example: Monolith vs Microservices.

![img_4.png](../files/data_engineering/img_4.png)

### Greenfield vs Brownfield Architecture

- Greenfield: A New system that is being built from scratch.
- Brownfield: An exiting system that is being updated or modified.
- Evaluate the trade-offs of each approach.

## Source Systems

- Common examples of Source systems:
  - Databases
  - APIs
  - Message queues and event-streaming platforms.

### Databases

- A Database is a collection of data that is organized and stored for efficient retrieval and manipulation.
- Common types of database source systems:
  - Relational Database
  - NoSQL
    - Key-value
    - Document
    - Wide-Column
    - Graph
- Relational Database:
  - A Table structured with rows and columns.
  - Predefined schema.
  - Row: represents a single record.
  - Column: represents an attribute.
  - Keys: Primary and Foreign Key.
  - Interface is often SQL.
- NoSQL
  - Flexible Data Model.
  - Fast Data Access.
  - Great for simple queries.

### APIs
  - API: Application Programming Interface
  - Used to access data from applications or 3rd parties.
  - Common types of APIs
    - REST
      - Popular protocol
    - GraphQL
      - Specify exactly what data you need from the server, without having to make multiple requests.

### Message Queues and Event-Streaming Platforms
  - Message Queue
    - Asynchronously send small messages between discrete services using a publish and subscribe model.
    - Useful for decoupling services from each other.
  - Event-Streaming Platform
    - Similar to message queue, but used to ingest and process data in an ordered log of records.
    - Producers send events to topics, which are consumed by subscribers.

### Undercurrents for Storage
- Security: Data encrypted at rest and during transmission, keep API keys and database passwords secret.
- Data Management: Understand how data is managed in the source system.
- DataOps: Clearly communicate with stakeholders and set up observability.
- Data Architecture: Understand upstream architecture.
- Orchestration: Make Sure orchestration and dependencies can access the source system.

## Ingestion

- Process of moving data from one place to another.
- "A Data Pipeline is the combination of architecture, systems and processes that move data through the stages of the data engineering lifecycle."
- Key Concepts for Data Ingestion:
  - Bounded vs Unbounded Data.
  - Batch vs Streaming.
  - Sync vs Async.
  - Push vs Pull.
  - Schema Changes.

### Bounded vs Unbounded

![img_5.png](../files/data_engineering/img_5.png)

- Unbounded: Data continuously flows.
- Bounded: Bucketing data, dividing into chunks for processes.

### Batch vs Streaming

- Batch: Fixed Intervals (data size or time based)
- Streaming: Continuously flowing data
- Most of the time, Streaming and Real-time are used interchangeably.

### Schema Changes

- What happens if the schema in your source system changes?
- Pipelines might break...
- Especially problematic: column deletion or column name changes.
- Solutions:
  - Observability
  - Data Contracts.
  - Communicate with source system stakeholders.


### Undercurrents

- Security: Encryption in transit and at rest.
- Data Management: Schema changes, handling sensitive data.
- DataOps: Set up observability and monitoring for your datapipelines, data quality tests.
- Data Architecture: Build for resiliency and failure.
- Orchestration: Consider dependencies in your pipelines.
- Software Engineering: Avoid writing code that has a lot of tight dependencies.


## Transformations

- A Query allows you to retrieve and act on data.
- Types of query:
  - Select: Retrieve data
  - Action: Update or Delete data
- Life of a query: `SQL query issued -> Parsing and conversion to bytecode -> Query Planning and Optimization -> Query execution -> Results returned`
- Query Optimizer
  - Optimizes query performance.
  - Explain plan: Helpful for diagnosing queries.
    - Shows the execution plan chosen by the dataset optimizer for a specific query.
    - An execution plan is a sequence of steps that the database will take to execute the statement.
    - Useful for understanding performance issues with a query.
- Data Modeling
  - A Data model represents the way data relates to the real world.
  - A good data model captures how communication and work naturally flow within your organization.
  - A poor data model results in haphazard, confusing and incoherent data.
  - Often overlooked by data professionals.
  - Stages of Data Modeling:
    - Conceptual: High level understanding of how data and concepts relate. No technical detail.
    - Logical: Intermediate step of transforming the conceptual model into a structure.
    - Physical: Database implementation and optimization of the logical model.
  - Normalization
    - A good practice to make sure we have removed redundancies and understand the relationships in our data.
    - Especially helpful with relation databases.
    - Levels of normalization: 1NF, 2NF, 3NF, Boyce-Codd NF
    - Based on set theory and first order predicate logic.
    - Check Paper: https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf
- Analytical Data Modeling Approaches
  - Dimensional
  - Data Vault.
  - One Big Table (OBT)
  - Just a Bunch Of Tables (JBOT)
  - 'Query-driven modeling'
- Views
  - View: A Virtual table that is created from a query.
  - Materialized view: A Physical table that is created from a query.
- ELT vs ETL

### Undercurrents of Transformation

- Security: Principle of the least privileges to systems and data.
- Data Management: Data Privacy and Masking, Data Lineage, Data Model Integrity.
- DataOps: Data Quality and System Monitoring.
- Data Architecture: Ensure for easy querying and data processing.
- Orchestration: Event vs Time Based.
- Software Engineering: Write Clean code and make it easy to manage.

## Storage

- Phases of Storage.

![img_6.png](../files/data_engineering/img_6.png)

- Raw Ingredients
  - Disk storage types: HDD, SSD
  - RAM
  - CPU
  - Networking
  - Serialization
  - Compression
- Disk Storage vs RAM
  - Disk Storage
    - HDD: Hard disk drive
    - SSD: Solid-state drive
    - Slower data access than RAM
    - Non-volatile: Data is preserved when power is turned off.
  - RAM
    - Short-term memory
    - Fast data access
    - Volatile: Data is lost when power is turned off.
  - Common Storage Systems
    - RDBMS and other databases
    - Object Storage
    - Cache/memory-based
    - Streaming storage
    - HDFS - Hadoop File System
- Object Storage
  - Manages data as objects
  - Objects have
    - Data
    - Unique Identifier
    - Metadata
  - Extremely common for Data Engineering workloads
  - Popular Object storage: AWS S3, Azure Blob Storage, GCP Cloud Storage

![img_7.png](../files/data_engineering/img_7.png)

  - Object Storage has varying costs associated with different storage tiers
    - AWS S3
      - Regular (hot): $0.02/GB
      - Infrequent Access (warm): $0.01/GB
      - Glacier (Cold): $0.004/GB

- Storage Abstractions
  - Data Warehouse
  - Data Lake
  - Data Lakehouse
  - Data Platform
- Data Warehouse
  - A Data warehouse is a "subject-oriented, non-volatile, integrated, time-variant collection of data in support of management's decision."
  - Goal: Separate Analytical and Transactional workloads.
  - Extremely common in organizations of all sizes.
  - Components of Data Warehouse:
    - Operational Source System
    - ETL: Extract, transform, and Load
    - Data mart
    - Data Warehouse

![img_8.png](../files/data_engineering/img_8.png)

![img_9.png](../files/data_engineering/img_9.png)

### Undercurrents of Storage

- Security: Encryption at rest, Role based access control, column and row-level protection.
- Data Management: Data Catalogs, Data Versioning, Privacy
- DataOps: Monitoring and observability
- Data Architecture: Build for resiliency and failure.
- Orchestration: "Storage allows data to flow through pipelines, and orchestration is the pump."
- Software Engineering: Performant code and avoid coupling your code to storage. (Separate compute and Storage)

## Serving

- Data Engineering isn't done in a vacuum. Serving data ties data back to business use cases and adding value.
- Use cases: Analytics, Machine Learning and Reverse ETL.

### Analytics

- Analytics is the process of collecting, analyzing and interpreting data to gain insights that can be used to make better decisions.
- Goal is to turn data data into actionable insights.
- Business intelligence (BI)
  - Provides insights into the past and present.
  - Reports and dashboards
- Ad hoc analysis
  - Exploratory Data Analysis.
  - One-time answers.
- Business vs Operational Analytics
  - Business Analytics: Analyzing Historical data to glean insights, identify trends, and guide strategic decisions for long-term planning.
  - Operational Analytics: Real-time monitoring and optimization of business operations.
- Machine Learning
  - ML algorithms are trained on data, and then they can use that data to make predictions or decisions.
  - Things to know:
    - Difference between supervised and unsupervised learning.
    - Understand the basics of deep learning and 'classical' techniques.
    - Various approaches for different types of data:
      - Tabular Data: XGBoost, 'classical' techniques.
      - Unstructured Data: Various Generative AI Approaches.
- Reverse ETL

![img_10.png](../files/data_engineering/img_10.png)

### Undercurrents of Serving.

- Security: Principle of the least privilege to systems and data.
- Data Management: Build TRUST in the data you serve.
- DataOps: Data Quality and Serving Monitoring.
- Data Architecture: Ensure for easy querying and data processing.
- Orchestration: Event vs Time-based.
- Software Engineering: Write Clean code and make it easy to manage.