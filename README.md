import json
import boto3
client = boto3.client('sns')
def lambda_handler(event, context):
    response = client.publish(TopicArn='arn:aws:sns:us-east-1:526312876991:mobmail',Message="This is a Test Message from MobMail")
    print("Message published")
    return(response)
