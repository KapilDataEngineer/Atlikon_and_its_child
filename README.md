# Atlikon_and_its_child
step by step flow 

1. understand the business and requirement
   
2. Existing ATLIKON parent company model
   1.We have 4 dimension table and 1 fact table in the OLAP model
   2. These  table constitute a star schema
   3. Let say today is 9th november and we will go live in evening
   4. ATLIKON also have its child company and have its OLTP db setup
   5. We want to merge child company data to parent company for serving a single platform for analytics
   6. Till 9th november there will initial load of child company but after that incremental load will run daily and parent and child company          will be in sync
   7. for ease of coding we have local csv files for parent company data till 9th november, and the data is already in gold format for olap           model
   8. we need to build pipeline for child company to convert oltp system to olap.

2.1 => Questions 
1. As we are building data model in databricks
   what is unity catalog
   how do you manage access
   what is metastore
   where is data stored physically

3.Child company 
  1.the data files for child company is sitting in s3 bucket
  2.we will create databricks external connection to s3 bucket 
  3.Understand how the connection is established
  4.create the data pipeline bronze-silver-gold
  5. keep in mind that as you have to merge the data finally with parent company we need to get alligned to parent company structure
  
   
