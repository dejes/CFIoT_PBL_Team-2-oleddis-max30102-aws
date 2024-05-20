# CFIoT_PBL_Team-2-oleddis-max30102-aws

This docs explain how to set up IoT rules to publish data to DynamoDB.

1. Create table in DynamoDB
   ![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/createTable1.png)

   Set t(time) as Partition Key, beat as Sort Key.

2. Navigate to AWS IoT/Message routing/Rules
   ![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/iotCoreRules1.png)

3. Create rule
![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/iotCoreRules2.png)

4. Fill in Rule name then go to next step
![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/iotCoreRules3.png)

5. Set up SQL statement
   SELECT t,beat FROM 'esp32/pub'
   ![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/iotCoreRules4.png)

6. Set up Rule actions
   *Select DynamoDBv2
   *Choose the Table you create in Step 1
   *Choose IAM role "LabRole"
   *Click Next
   ![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/iotCoreRules5.png)

7. Click create to finish set up
   ![alt text](https://github.com/dejes/CFIoT_PBL_Team-2-oleddis-max30102-aws/blob/main/connect_to_db_screenshots/iotCoreRules6.png)
   
