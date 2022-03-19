# cloudformation
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
AWS::AccountId
AWS::StackName
AWS::NoValue  --> Very Important when using Conditions
```
