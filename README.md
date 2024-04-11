# Chat App

This repository contains the source code for a chat application.

## Environment Variables

Before deploying the application, make sure to add the following environment variables to your deployment platform:

- `BUCKETEER_AWS_ACCESS_KEY_ID=` _(Your AWS Access Key ID)_
- `BUCKETEER_AWS_SECRET_ACCESS_KEY=` _(Your AWS Secret Access Key)_
- `BUCKETEER_BUCKET_NAME=` _(Your AWS S3 Bucket Name)_
- `JWT_SECRET=` _(Your JWT Secret for authentication)_
- `MONGO_URL=` _(URL for your MongoDB database)_
- `NODE_ENV=` _(Environment mode: "production" or "development")_
- `PORT=3001` _(Port number for the server)_
- `VITE_APP_API_URL=` _(URL for your API endpoint)_

## AWS S3 Configuration

### CORS Configuration:

```json
[
    {
        "AllowedHeaders": [
            "*"
        ],
        "AllowedMethods": [
            "GET",
            "PUT",
            "POST",
            "HEAD",
            "DELETE"
        ],
        "AllowedOrigins": [
            "*"
        ],
        "ExposeHeaders": [],
        "MaxAgeSeconds": 3000
    }
]
```

### Bucket Policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::justanotheridiotbucket/*"
    }
  ]
}
```

---

Make sure to replace the placeholder values with your actual credentials and configuration details before deploying the application.
