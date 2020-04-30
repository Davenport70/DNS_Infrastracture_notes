# Auto Scaling

## What is Auto Scaling?

AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.

## How does it work?

Launch Configurations hold the instructions for the creation of new instances. The instructions describe what type of instance AutoScaling needs to launch (e.g. t2.medium, m3.large), what Amazon Machine Image (AMI) the new instance is going to be based on, what roles or what storage is going to be associated with the instance, and so on.

Scaling Groups, on the other hand, manage the scaling rules and logic, which are defined in policies. Those could be based on schedule or CloudWatch metrics. The CloudWatch service allows you to monitor all resources and applications that you have deployed on AWS. CloudWatch allows you to define alarms on metrics, which the AutoScaling policies subscribe to.

## Example of Terraform Autoscaling

```
resource "aws_autoscaling_group" "bar" {
  availability_zones = ["us-east-1a"]
  desired_capacity   = 1
  max_size           = 1
  min_size           = 1

  launch_template {
    id      = "${aws_launch_template.foobar.id}"
    version = "$Latest"
  }
}
```

**Author**

**Zack Davenport** - *Junior DevOps Engineer* - Davenport70
