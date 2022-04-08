# cloudformation
Source - https://github.com/stacksimplify/aws-cloudformation-simplified
```
Resources   --> 
Parameters  --
Mappings
Conditions
Outputs
Metadata  Two types of Metadata - 1) Designer 2) Interface
```

Base Template
Source - 
```
Metadata Format
    |
Packages
groups
users
sources
files
Commands --> service --> Helper scripts -> aws-cfn-bootstrap -> cfn-init -> cfn-signal -> outputs -> Create Stack and Test
```
Intrinsic Functions
```
Fn::Ref
Fn::Base64
Fn::FindInMap
Fn::Join
...etc
```
Condition Functions
```
Fn::ANd
Fn::Equals
Fn::If
Fn::Not
Fn::Or
```
Pseudo Parameters
```
AWS::Region
AWS::StackName
AWS::NoValue  --> Very Important when using Conditions
AWS::NotificationARNs
AWS::AccountId
Returns the AWS account ID of the account in which the stack is being created, such as 123456789012.

AWS::NotificationARNs
Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

AWS::Partition
Returns the partition that the resource is in. For standard AWS Regions, the partition is aws. For resources in other partitions, the partition is aws-partitionname. For example, the partition for resources in the China (Beijing and Ningxia) Region is aws-cn and the partition for resources in the AWS GovCloud (US-West) region is aws-us-gov.

AWS::Region
Returns a string representing the Region in which the encompassing resource is being created, such as us-west-2.

AWS::StackId
Returns the ID of the stack as specified with the aws cloudformation create-stack command, such as arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123.

AWS::StackName
Returns the name of the stack as specified with the aws cloudformation create-stack command, such as teststack.

AWS::URLSuffix
Returns the suffix for a domain. The suffix is typically amazonaws.com, but might differ by Region. For example, the suffix for the China (Beijing) Region is amazonaws.com.cn.
```

Yaml Basics
```
  Key value pairs -> 
      Name: Niranjan
      Age: 30
      Occupation: Engineer
      Team: DevOps
      State: 'Talangana India'
```
Lists or Ayyars - Indented with 'Dash', Dash indicayes thats a element of an Array.
```
Block Sequence
Persons: 
  - Niranjan
  - Rishi
  - Ram
  - Laxman
  
Flow Sequence: 
person: [Niranjna, Rishi, Ram Laxman]
```
Dictionary
```
Yaml Dictionaries are set of properties grouped together under an item, dictionary contain key value pairs.
Niranjan: 
  Age: 30
  gender: male
  Team: Devops
```
YAML Lists containing Dictionaries.
```
Persons: 
  - Dave: 
      Age: 25
      Occupation: Engineer
      State: California
  - John: 
      Age: 25
      Occupation: Plumber
      State: Florida
  - Mike: 
      Age: 30
      Occupation: Carpenter
      State: Texas
```
Lists containing Dictionaries Containing Lists
```
Persons: 
  - Dave: 
      Age: 25
      Occupation: Engineer
      State: California
      Degrees: 
        - Bachelars
        - Masters
        - Phd
  - John: 
      Age: 25
      Occupation: Plumber
      State: Florida
      Degrees: 
        - Bachelars
        - Masters
        - Phd
  - Mike: 
      Age: 30
      Occupation: Carpenter
      State: Texas
      Degrees: 
        - Bachelars
        - Masters
        - Phd
```
Pipe -> The Pipe notation also reffered to as Literal Block, All new lines indentation extra spaces everything preserved as is.
```
- Mike: 
      Age: 30
      Occupation: Carpenter
      State: Texas
      Address: |
        Flat 402 uppal
        Hydearabad Telangana
        pincode 500039
```
Greater Than symbal - The greater than sign notation also reffered to as folded Block, 
Renders the test as single line
All New lines will be replaced with a single Space
Blan lines are converted to a new line character.
```
- Mike: 
      Age: 30
      Occupation: Carpenter
      State: Texas
      AboutMe: >
        Hello mysel Niranjan
        Hydearabad Telangana
        pincode 500039
```
Comments
```
# used for comments
```
Intrinsic
```
AWS::EC2::Instance
       AvailabilityZone
       PrivateDnsName
       PrivateIp
       PublicDnsName
       PublicIp
```
Metadata
```
   Three types of Metadata..
    AWS::CloudFormation::Designer
    AWS::CloudFormation::Interface
    AWS::CloudFormation::Init
```
