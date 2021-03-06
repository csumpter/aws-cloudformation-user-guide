# AWS::AppMesh::VirtualNode GrpcTimeout<a name="aws-properties-appmesh-virtualnode-grpctimeout"></a>

An object that represents types of timeouts\. 

## Syntax<a name="aws-properties-appmesh-virtualnode-grpctimeout-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-grpctimeout-syntax.json"></a>

```
{
  "[Idle](#cfn-appmesh-virtualnode-grpctimeout-idle)" : [Duration](aws-properties-appmesh-virtualnode-duration.md),
  "[PerRequest](#cfn-appmesh-virtualnode-grpctimeout-perrequest)" : [Duration](aws-properties-appmesh-virtualnode-duration.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-grpctimeout-syntax.yaml"></a>

```
  [Idle](#cfn-appmesh-virtualnode-grpctimeout-idle): 
    [Duration](aws-properties-appmesh-virtualnode-duration.md)
  [PerRequest](#cfn-appmesh-virtualnode-grpctimeout-perrequest): 
    [Duration](aws-properties-appmesh-virtualnode-duration.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-grpctimeout-properties"></a>

`Idle`  <a name="cfn-appmesh-virtualnode-grpctimeout-idle"></a>
An object that represents an idle timeout\. An idle timeout bounds the amount of time that a connection may be idle\. The default value is none\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-virtualnode-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PerRequest`  <a name="cfn-appmesh-virtualnode-grpctimeout-perrequest"></a>
An object that represents a per request timeout\. The default value is 15 seconds\. If you set a higher timeout, then make sure that the higher value is set for each App Mesh resource in a conversation\. For example, if a virtual node backend uses a virtual router provider to route to another virtual node, then the timeout should be greater than 15 seconds for the source and destination virtual node and the route\.  
*Required*: No  
*Type*: [Duration](aws-properties-appmesh-virtualnode-duration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)