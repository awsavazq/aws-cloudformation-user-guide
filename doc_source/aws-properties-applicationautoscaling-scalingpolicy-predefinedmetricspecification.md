# AWS::ApplicationAutoScaling::ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification"></a>

 `PredefinedMetricSpecification` is a subproperty of [TargetTrackingScalingPolicyConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.html) that configures a predefined metric for a target tracking scaling policy to use with Application Auto Scaling\. 

For more information, see [PredefinedMetricSpecification](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PredefinedMetricSpecification.html) in the *Application Auto Scaling API Reference*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax.yaml"></a>

```
  [PredefinedMetricType](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype): String
  [ResourceLabel](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-properties"></a>

`PredefinedMetricType`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype"></a>
The metric type\. The `ALBRequestCountPerTarget` metric type applies only to Spot fleet requests and ECS services\.   
*Required*: Yes  
*Type*: String  
*Allowed Values*: `ALBRequestCountPerTarget | AppStreamAverageCapacityUtilization | CassandraReadCapacityUtilization | CassandraWriteCapacityUtilization | ComprehendInferenceUtilization | DynamoDBReadCapacityUtilization | DynamoDBWriteCapacityUtilization | EC2SpotFleetRequestAverageCPUUtilization | EC2SpotFleetRequestAverageNetworkIn | EC2SpotFleetRequestAverageNetworkOut | ECSServiceAverageCPUUtilization | ECSServiceAverageMemoryUtilization | LambdaProvisionedConcurrencyUtilization | RDSReaderAverageCPUUtilization | RDSReaderAverageDatabaseConnections | SageMakerVariantInvocationsPerInstance`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBRequestCountPerTarget` and there is a target group attached to the Spot Fleet request or ECS service\.  
The format is app/<load\-balancer\-name>/<load\-balancer\-id>/targetgroup/<target\-group\-name>/<target\-group\-id>, where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification--seealso"></a>
+ [Target Tracking Scaling Policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html) in the *Application Auto Scaling User Guide* 