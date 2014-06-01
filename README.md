# awssum-amazon-sqs #

This is an ```AwsSum``` plugin!

You'll need to add [awssum-amazon-sqs](https://github.com/awssum/awssum-amazon-sqs/) to your package.json
dependencies. Both [awssum](https://github.com/awssum/awssum/) and
[awssum-amazon](https://github.com/awssum/awssum-amazon/) are pulled in as peer dependencies.

## Example ##

List all your alarms:

```
var fmt = require('fmt');
var amazon = require('awssum-amazon');
var amazonSqs = require('awssum-amazon-sqs');

var sqs = new amazonSqs.Sqs({
    'awsAccountId'    : '...',
    'accessKeyId'     : process.env.ACCESS_KEY_ID,
    'secretAccessKey' : process.env.SECRET_ACCESS_KEY,
    'region'          : amazon.US_EAST_1
});

sqs.ListQueues(function(err, data) {
    fmt.dump(err, 'err');
    fmt.dump(data, 'data');
});
```

## Operations ##

### AddPermission ###

Docs: [AddPermission on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryAddPermission.html)

### ChangeMessageVisibility ###

Docs: [ChangeMessageVisibility on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryChangeMessageVisibility.html)

### ChangeMessageVisibilityBatch ###

Docs: [ChangeMessageVisibilityBatch on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryChangeMessageVisibilityBatch.html)

### CreateQueue ###

Docs: [CreateQueue on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryCreateQueue.html)

### DeleteMessage ###

Docs: [DeleteMessage on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryDeleteMessage.html)

### DeleteMessageBatch ###

Docs: [DeleteMessageBatch on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryDeleteMessageBatch.html)

### DeleteQueue ###

Docs: [DeleteQueue on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryDeleteQueue.html)

### GetQueueAttributes ###

Docs: [GetQueueAttributes on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryGetQueueUrl.html)

### GetQueueUrl ###

Docs: [GetQueueUrl on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryGetQueueAttributes.html)

### ListQueues ###

Docs: [ListQueues on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryListQueues.html)

### ReceiveMessage ###

Docs: [ReceiveMessage on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryReceiveMessage.html)

### RemovePermission ###

Docs: [RemovePermission on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QueryRemovePermission.html)

### SendMessage ###

Docs: [SendMessage on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QuerySendMessage.html)

### SendMessageBatch ###

Docs: [SendMessageBatch on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QuerySendMessageBatch.html)

### SetQueueAttributes ###

Docs: [SetQueueAttributes on AWS](http://docs.amazonwebservices.com/AWSSimpleQueueService/latest/APIReference/Query_QuerySetQueueAttributes.html)



# Author #

Written by [Andrew Chilton](http://chilts.org/) - [Blog](http://chilts.org/blog/) -
[Twitter](https://twitter.com/andychilton).

# License #

* [Copyright 2011-2013 Apps Attic Ltd.  All rights reserved.](http://appsattic.mit-license.org/2011/)
* [Copyright 2013 Andrew Chilton.  All rights reserved.](http://chilts.mit-license.org/2013/)

(Ends)
