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
AWS::AccountId
AWS::StackName
AWS::NoValue  --> Very Important when using Conditions
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
