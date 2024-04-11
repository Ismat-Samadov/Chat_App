add this environment variable to your deploy platform
BUCKETEER_AWS_ACCESS_KEY_ID=
BUCKETEER_AWS_SECRET_ACCESS_KEY=
BUCKETEER_BUCKET_NAME=
JWT_SECRET=
MONGO_URL=
NODE_ENV=
PORT=3001
VITE_APP_API_URL=

update AWS S3 BUCKET CORS and  Bucket policy

CORS: 
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

Bucket policy:
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