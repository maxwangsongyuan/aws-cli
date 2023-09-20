### **AWS S3 CLI Operations**

---

**Bucket Operations:**

- **Create a Bucket:** 
  ```
  aws s3api create-bucket --bucket BUCKET-NAME
  ```

- **List all Buckets:** 
  ```
  aws s3api list-buckets --query "Buckets[].Name"
  ```

- **Delete a Bucket:** 
  ```
  aws s3api delete-bucket --bucket BUCKET-NAME
  ```

---

**Object Operations:**

- **Copy Objects:** 
  ```
  aws s3 cp SOURCE DEST
  ```

- **Move Objects:** 
  ```
  aws s3 mv SOURCE DEST
  ```

- **Delete Objects:** 
  ```
  aws s3 rm PATH
  ```

- **List Objects in a Bucket:** 
  ```
  aws s3api list-objects --bucket BUCKET-NAME --query "Contents[].Key" --region REGION
  ```

- **Retrieve Metadata from an Object:** 
  ```
  aws s3api head-object --bucket BUCKET-NAME --key OBJECT-KEY
  ```

- **Get a Specific Version of an Object:** 
  ```
  aws s3api get-object --bucket BUCKET-NAME --key OBJECT-KEY --version-id VERSION-ID OUTPUT-FILE
  ```

- **Get the ACL of an Object:** 
  ```
  aws s3api get-object-acl --bucket BUCKET-NAME --key OBJECT-KEY
  ```

- **Set the ACLs of an Object:** 
  ```
  aws s3api put-object-acl --bucket BUCKET-NAME --key OBJECT-KEY --acl ACL-VALUE
  ```

---

**Directory Operations:**

- **List Objects in a Directory:** 
  ```
  aws s3 ls s3://BUCKET-NAME/PATH
  ```

- **Sync Directories:** 
  ```
  aws s3 sync SOURCE DEST
  ```

---

**Bucket Policy and Permissions:**

- **Retrieve Bucket Policies:** 
  ```
  aws s3api get-bucket-policy --bucket BUCKET-NAME
  ```

- **Apply a Policy from a File to a Bucket:** 
  ```
  aws s3api put-bucket-policy --bucket BUCKET-NAME --policy FILE-NAME
  ```

---

**Object Versioning:**

- **Enable Versioning on a Bucket:** 
  ```
  aws s3api put-bucket-versioning --bucket BUCKET-NAME --versioning-configuration Status=Enabled
  ```

---

