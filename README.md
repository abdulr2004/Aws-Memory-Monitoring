# Aws-Memory-Monitoring
Features:
I set up an EC2 instance using Amazon Linux 2, making sure it was secure by customizing the security group and limiting SSH access. I also created a new user with sudo rights, disabled root login, and required key-based SSH authentication for increased security. Finally, I configured CloudWatch alarms to track CPU usage and send alerts if it goes over a set limit.

Commands Used to configure cloudwatch:

1. sudo apt-get update
2. wget https://s3.amazonaws.com/amazoncloudw...
3. sudo dpkg -i amazon-cloudwatch-agent.deb
4. sudo apt-get install -f
5. sudo amazon-cloudwatch-agent-ctl -a status
6. sudo amazon-cloudwatch-agent-ctl -a start -m ec2 -c file:/opt/aws/amazon-cloudwatch-agent/etc/amazon-cloudwatch-agent.json -s   
7. sudo amazon-cloudwatch-agent-ctl -a stop -m ec2 
8. sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard  
9. sudo amazon-cloudwatch-agent-ctl -a start -m ec2 -c file:/opt/aws/amazon-cloudwatch-agent/etc/amazon-cloudwatch-agent.json -s
