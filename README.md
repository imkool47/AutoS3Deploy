# AutoS3Deploy
Objective: Automate the deployment of a static website from a GitHub repository to an Amazon S3 bucket using GitHub Actions.
Prerequisites:

    1. GitHub Repository: A repository containing the static website's source code.

    2. AWS S3 Bucket: An S3 bucket configured to host a static website.

    3. AWS IAM User: An IAM user with the necessary permissions to access and upload to the S3 bucket.

Steps:

    1. Setup AWS Credentials:
        Create an IAM user with AmazonS3FullAccess.
        Generate Access Key ID and Secret Access Key for the IAM user.

    2. Store AWS Credentials in GitHub Secrets:
        Navigate to your GitHub repository.
        Go to Settings > Secrets and variables > Actions.
        Add the following secrets:
            AWS_ACCESS_KEY_ID
            AWS_SECRET_ACCESS_KEY
            AWS_REGION (e.g., us-east-1)
            S3_BUCKET_NAME (name of your S3 bucket)

    3. Create GitHub Actions Workflow:
        Create a .github/workflows/deploy.yml file in your repository.

    4. Trigger Deployment:

    Push your changes to the main branch.
    The GitHub Actions workflow will trigger and deploy your static website to the specified S3 bucket.