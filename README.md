s3-account-copy
===
Provides a quick and easy way to safely copy AWS S3 buckets from one account to another using Cloudformation and the AWS CLI.

##Instructions
Follow the instructions below to copy date from an S3 bucket in the "source" account to an S3 bucket in the "destination" account.

1. In the destination account, run the destination-account.cf Cloudformation template.

2. In the source account, run the source-account.cf Cloudformation template.

3. Using the AccessKeyId and the AccessSecretKey from the s3_copy_user created in the destination account run the following command:

	```
	aws s3 cp s3://{source S3 bucket name} s3://{destination S3 bucket name} --recursive
	```

## Bugs and Feedback
For bugs, questions and discussions please use the [Github Issues](https://github.com/gregwhitaker/s3-account-copy/issues).

##License
Copyright 2016 Greg Whitaker

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
