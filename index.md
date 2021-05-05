Cross-origin resource sharing (CORS)
[
    {
        "AllowedHeaders": [
            "*"
        ],
        "AllowedMethods": [
            "GET",
            "PUT",
            "POST",
            "DELETE",
            "HEAD"
        ],
        "AllowedOrigins": [
            "https://aletha.s3.us-east-2.amazonaws.com",
            "http://aletha.s3-website.us-east-2.amazonaws.com",
            "https://s3.amazonaws.com"
        ],
        "ExposeHeaders": [
            "ETag",
            "x-amz-meta-myheader",
            "x-amz-meta-custom-header",
            "x-amz-server-side-encryption",
            "x-amz-request-id",
            "x-amz-id-2",
            "date"
        ],
        "MaxAgeSeconds": 3000
    }
]
Bucket policy
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllPermissionsForOwner",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::aletha-site-public/*"
        }
    ]
}