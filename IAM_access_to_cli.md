
### Creating an IAM User for AWS CLI Access

#### Steps:

1. **Sign in to the AWS Management Console:**
   - Open the AWS Management Console at [https://aws.amazon.com/](https://aws.amazon.com/).
   - Sign in with your AWS account credentials.

2. **Add a New User:**
   - In the IAM dashboard, click on "Users" in the left-hand navigation pane.
   - Click the "Add user" button.

3. **Set User Details:**
   - Enter a user name for the new user. This can be any name you choose.
   
4. **Assign Permissions:**
   - Click "Next: Permissions."
   - Select "Attach existing policies directly."
   - In the search box, type "AdministratorAccess" and check the corresponding box to attach the policy granting full access to all AWS services and resources.

5. **Review and Create User:**
   - Click "Next: Tags" to add optional tags to the user for organization and management purposes.
   - Click "Next: Review" to review the user's details and permissions.
   - Click "Create user" to create the user.

6. **Create Access Keys:**
   - After creating the user, go to the "Users" section in the IAM dashboard and select the newly created user.
   - Click on the "Security credentials" tab.
   - Scroll down to the "Access keys" section and click "Create access key."
   - The system will generate an access key ID and a secret access key. Download these credentials as a CSV file by clicking the "Download .csv" button.
   - **Important:** Store these credentials securely. You will not be able to view the secret access key again after you leave this page.

### Step 2: Configure AWS CLI with the New User

1. **Install AWS CLI:**
   - If you haven't already installed the AWS CLI, follow the instructions here: [Installing the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

2. **Configure the AWS CLI:**
   - Open your terminal or command prompt.
   - Run the following command to configure the AWS CLI with the new user's credentials:
     ```sh
     aws configure
     ```
   - Enter the access key ID and secret access key when prompted.
   - Specify the default region name (e.g., `us-east-1`).
   - Specify the default output format (e.g., `json`).

### Step 3: Verify the Configuration

1. **Verify the Configuration:**
   - Run a simple AWS CLI command to verify that the configuration is correct and the new user has the necessary permissions. For example:
     ```sh
     aws s3 ls
     ```
   - If the command executes successfully and returns a list of S3 buckets, the configuration is correct.

### Documentation Template

#### Creating an IAM User for AWS CLI Access

**Steps:**

1. Sign in to the AWS Management Console.
2. Navigate to IAM service.
3. Add a new user with programmatic access.
4. Assign "AdministratorAccess" policy.
5. Review and create the user.
6. Create access keys under the "Security credentials" tab.
7. Download the credentials (access key ID and secret access key).

**Configuring AWS CLI:**

1. Install AWS CLI.
2. Run `aws configure` in the terminal.
3. Enter the access key ID and secret access key.
4. Specify the default region and output format.

**Verification:**

1. Run a test AWS CLI command (e.g., `aws s3 ls`).

By following these steps, you should be able to create an IAM user with programmatic access, configure the AWS CLI, and verify the configuration to ensure everything is set up correctly. If you need further assistance or have additional requirements, feel free to ask!
