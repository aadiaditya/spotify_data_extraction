## spotify_data_extraction

![1707115057330](https://github.com/aadiaditya/spotify_data_extraction/assets/64732573/0c6d9572-c3e5-4988-b9fb-b2ae91671f97)

## Highlights:
- Integrated Spotify API to extract and analyze data using Python and Jupyter Notebooks
- Deployed extraction code on AWS Lambda, leveraging serverless computing
- Automated data extraction every minute using AWS CloudWatch triggers
- Implemented a transformation function and orchestrated S3 events for seamless data loading
- Organized files on S3 and built analytics tables using AWS Glue and Athena
- Explored integration between S3 and Snowflake via Snowpipe
 
## Results and Learnings:
- Tackled JSON data formats and delved into AWS services like Lambda
- Learned intricacies of event triggering, IAM roles for security, and optimal data organization on S3
- Satisfying experience integrating transformed files in S3 with Snowflake through Snowpipe

# Spotify ETL Project

This project aims to extract data from Spotify playlists using the Spotify API, transform it, and load it into an S3 bucket. The project is built using AWS Lambda, Spotify API, and the boto3 library for S3 interactions.

## Project Overview
The project consists of two main AWS Lambda functions:
1. **Extract and Load**: This function extracts data from a Spotify playlist and loads the raw JSON data into an S3 bucket.
2. **Transform and Load**: This function processes the raw JSON data, transforms it into CSV format, and loads the transformed data back into the S3 bucket.

## Features
- Extracts data from a specified Spotify playlist.
- Stores raw data in an S3 bucket.
- Transforms raw JSON data into structured CSV files.
- Loads transformed data into separate S3 folders for songs, albums, and artists.
- Moves processed raw files to a `processed` folder in the S3 bucket.

## Installation
To set up this project, you need to have AWS Lambda configured with appropriate permissions to access S3 and the Spotify API. You also need to set up environment variables for your Spotify client credentials.

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/spotify-etl-project.git
    cd spotify-etl-project
    ```

2. Set up AWS Lambda with the following environment variables:
    - `client_id`: Your Spotify API client ID.
    - `client_secret`: Your Spotify API client secret.

## Usage
1. Deploy the Lambda functions using AWS Lambda console or AWS CLI.
2. Ensure that the S3 bucket exists and is specified correctly in the code.
3. Trigger the **Extract and Load** Lambda function to start the data extraction and loading process.
4. The **Transform and Load** Lambda function will process the data and load the transformed CSV files into the S3 bucket.

## Lambda Functions

### Extract and Load Function
This function extracts data from the specified Spotify playlist and loads the raw JSON data into an S3 bucket.

