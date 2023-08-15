# aws_transcribe

## Project Overview

In this project, we leverage Amazon Web Services to seamlessly transform MP3 audio files into text transcripts. The core components of the project include:

- **Amazon S3:** The storage backbone where MP3 audio files are uploaded and trigger the automation process.
- **AWS Lambda:** Serverless functions that are invoked by S3 events, initiating the transcription workflow.
- **Amazon Transcribe:** The AI-powered service that performs audio-to-text transcription with impressive accuracy.

## Features

- **Automated Transcription:** Audio files uploaded to the designated S3 bucket trigger the transcription workflow without manual intervention.
- **Searchable Content:** The transcribed text can be indexed, allowing for efficient content searches within audio recordings.
- **Accessibility Enhancement:** The project enhances accessibility by making audio content available in textual form.

## Getting Started

**Prerequisites:** Ensure you have an AWS account.


**Step 1: Set Up Amazon S3**

1.Log in to your AWS Management Console.

2.Navigate to the Amazon S3 service.

3.Create a new S3 bucket where you will upload your MP3 audio files. Note the bucket name for later use.

**Step 2: Create an AWS Lambda Function**

1.Go to the AWS Lambda service from the AWS Management Console.

2.Click "Create function" and choose "Author from scratch."

3.Provide a name for your function, select a runtime (Python), and choose an execution role with permissions to access S3 and interact with Transcribe.

4.In the function code, write the logic to handle the S3 trigger event. When a new MP3 file is uploaded to the designated S3 bucket, this Lambda function will be invoked.

**Step 3: Configure S3 Event Trigger for Lambda**

1.In your Lambda function configuration, add a trigger by selecting the S3 bucket you created in Step 1.

2.Specify the event type that triggers the Lambda function (e.g., "Object Created (All)").

3.Configure suffix settings to .mp3, to narrow down the triggering events.

**step4: Upload**: upload an mp3 file in s3 bucket. You can see a transcription jon created in Amazon Transcribe .

**Step 5: Amazon Transcribe**
Navigate to the Amazon Transcribe service from the AWS Management Console.

you can download the transcribed file from s3 transcripts folder.

