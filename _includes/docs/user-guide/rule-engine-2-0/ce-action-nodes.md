Action Nodes execute various actions based on incoming Message.

* TOC
{:toc}

## Math Function Node

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 3.4.2</em></strong></td>
     </tr>
   </thead>
</table> 

The rule node applies math function and saves the result into the message and/or database. See table of supported functions below:

<style>

  div.mathFunctionsTable + table tr th:nth-child(1) {
     width: 10%
  }

  div.mathFunctionsTable + table tr th:nth-child(2) {
     width: 10%
  }

  div.mathFunctionsTable + table tr th:nth-child(3) {
     width: 65%
  }

  div.mathFunctionsTable + table tr th:nth-child(4) {
     width: 15%
  }

</style>

<div class="mathFunctionsTable"></div>

| Function | Number of arguments | Description   | Reference
|-----------|---|-------------|--------|
| ADD       | 2 | x + y       | |
| SUB       | 2 | x - y       | |
| MULT      | 2 | x * y       | |
| DIV       | 2 | x / y       | |
| SIN       | 1 | Returns the trigonometric sine of an angle.      | [Math.sin](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#sin(double))|
| SINH      | 1 | Returns the hyperbolic sine of a double value. The hyperbolic sine of x is defined to be (*e*<sup>x</sup> - *e*<sup>-x</sup>)/2 where *e* is Euler's number.     | [Math.sinh](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#sinh(double))|
| COS       | 1 | Returns the trigonometric cosine of an angle.       | [Math.cos](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#cos(double))|
| COSH      | 1 | Returns the hyperbolic cosine of a double value. The hyperbolic cosine of x is defined to be (*e*<sup>x</sup> + *e*<sup>-x</sup>)/2 where *e* is Euler's number.     | [Math.cosh](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#cosh(double))|
| TAN       | 1 | Returns the trigonometric tangent of an angle.      | [Math.tan](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#tan(double))|
| TANH      | 1 | Returns the hyperbolic tangent of a double value.      | [Math.tanh](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#tanh(double))|
| ACOS      | 1 | Returns the arc cosine of a value; the returned angle is in the range *0.0* through *pi*.     | [Math.acos](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#acos(double))|
| ASIN      | 1 | Returns the arc sine of a value; the returned angle is in the range *-pi/2* through *pi/2*.     | [Math.asin](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#asin(double))|
| ATAN      | 1 | Returns the arc tangent of a value; the returned angle is in the range -pi/2 through pi/2.     | [Math.atan](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#atan(double))|
| ATAN2     | 2 | Returns the angle theta from the conversion of rectangular coordinates (x, y) to polar coordinates (r, theta). | [Math.atan2](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#atan2(double,double))|
| EXP       | 1 | Returns the value *e*<sup>x</sup>, where *e* is the base of the natural logarithms.         |  [Math.exp](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#exp(double))|
| EXPM1     | 1 | Returns *e*<sup>x</sup>-1. Note that for values of x near 0, the exact sum of expm1(x) + 1 is much closer to the true result of *e*<sup>x</sup> than exp(x).            |  [Math.expm1](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#expm1(double)) |
| SQRT      | 1 | Returns the correctly rounded positive square root of a double value. | [Math.sqrt](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#sqrt(double))|
| CBRT      | 1 | Returns the cube root of a double value. | [Math.cbrt](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#cbrt(double))| 
| GET_EXP   | 1 | Returns the unbiased exponent used in the representation of a double.            |  [Math.getExponent](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#getExponent(double))|
| HYPOT     | 2 | Returns sqrt(x2 +y2) without intermediate overflow or underflow.   | [Math.getExponent](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#hypot(double,double)) |
| LOG       | 1 | Returns the natural logarithm (base e) of a double value. | [Math.log](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#log(double))|
| LOG10     | 1 | Returns the base 10 logarithm of a double value. |  [Math.log10](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#log10(double))  |
| LOG1P     | 1 | Returns the natural logarithm of the sum of the argument and 1. Note that for small values x, the result of log1p(x) is much closer to the true result of ln(1 + x) than the floating-point evaluation of log(1.0+x).            |  [Math.log1p](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#log1p(double))|
| CEIL      | 1 | Returns the smallest (closest to negative infinity) double value that is greater than or equal to the argument and is equal to a mathematical integer. |  [Math.ceil](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#ceil(double)) |
| FLOOR     | 1 | Returns the largest (closest to positive infinity) double value that is less than or equal to the argument and is equal to a mathematical integer. |  [Math.floor](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#floor(double)) |
| FLOOR_DIV | 2 | Returns the largest (closest to positive infinity) long value that is less than or equal to the algebraic quotient. |  [Math.floorDiv](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#floorDiv(long,long)) |
| FLOOR_MOD | 2 | Returns the floor modulus of the long arguments. |  [Math.floorMod](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#floorMod(long,long)) |
| ABS       | 1 | Returns the absolute value of a double value.             |  [Math.abs](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#abs(double)) |
| MIN       | 2 | Returns the smaller of two double values.            |  [Math.min](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#min(double,double)) |
| MAX       | 2 | Returns the greater of two double values.             |  [Math.max](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#max(double,double)) |
| POW       | 2 | Returns the value of the first argument raised to the power of the second argument.             |  [Math.pow](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#pow(double,double)) |
| SIGNUM    | 1 | Returns the signum function of the argument; zero if the argument is zero, 1.0 if the argument is greater than zero, -1.0 if the argument is less than zero.            |  [Math.signum](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#signum(double)) |
| RAD       | 1 | Converts an angle measured in degrees to an approximately equivalent angle measured in radians.             |  [Math.toRadians](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#toRadians(double)) |
| DEG       | 1 | Converts an angle measured in radians to an approximately equivalent angle measured in degrees.            |  [Math.toDegrees](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Math.html#toDegrees(double)) |
| CUSTOM    | 1-16| Use this function to specify complex math expressions. For example, transform Fahrenheit to Celsius using (x - 32) / 1.8) | [exp4j](https://github.com/fasseg/exp4j)  |

You may use 5 types of arguments:

 * Constant;
 * Value from the message body;
 * Value from the message meta data;
 * Value of the attribute that belongs to the message originator (device, asset, etc). Value should be of Numeric type or string that is convertible to float;
 * Value of the latest time-series that belongs to the message originator (device, asset, etc). Value should be of Numeric type or string that is convertible to float;

Primary use case for this rule node is to take one or more values from the database and modify them based on data from the message. For example, you may increase `totalWaterConsumption` based on the `deltaWaterConsumption` reported by device.

Alternative use case is the replacement of simple JS `script` nodes with more light-weight and performant implementation. For example, you may transform Fahrenheit to Celsius (*C = (F - 32) / 1.8*) using CUSTOM operation and expression: *(x - 32) / 1.8)*.

The execution is synchronized in scope of message originator (e.g. device) and server node. If you have rule nodes in different rule chains, they will process messages from the same originator synchronously in the scope of the server node.

The result of the function may be added to the message body or metadata. You may also save the result to the database as an attribute or time-series.


## Create Alarm Node

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-create-alarm.png)

This Node tries to load the latest Alarm with configured **Alarm Type** for Message Originator.
If **Uncleared** Alarm exist, then this Alarm will be updated, otherwise a new Alarm will be created.

Node Configuration:

- **Alarm Details Builder** script
- **Alarm Type** - any string that represents Alarm Type
- **Alarm Severity** - {CRITICAL \| MAJOR \| MINOR \| WARNING \| INDETERMINATE}
- is **Propagate** - whether Alarm should be propagated to all parent related entities.

Note: Since TB Version 2.3.0 the rule node has the ability to:

-  read alarm config from message:

-  get alarm type using pattern with fields from message metadata:

    ![image](/images/user-guide/rule-engine-2-0/nodes/action-create-alarm-config-from-msg.png)
  
Note: Since TB Version 2.4.3 the rule node has the ability to:

- filter propagation to parent entities by relation types:

    ![image](/images/user-guide/rule-engine-2-0/nodes/action-create-alarm-propagate-list.png)

**Alarm Details Builder** script used for generating Alarm Details JsonNode. It is useful for storing additional parameters
inside Alarm. For example you can save attribute name/value pair from Original Message payload or Metadata. 

**Alarm Details Builder** script should return **details** object.
 
![image](/images/user-guide/rule-engine-2-0/nodes/action-create-alarm-config.png)

- Message _payload_ can be accessed via <code>msg</code> property. For example <code>msg.temperature</code><br> 
- Message _metadata_ can be accessed via <code>metadata</code> property. For example <code>metadata.customerName</code><br> 
- Message _type_ can be accessed via <code>msgType</code> property. For example <code>msgType</code><br>

**Optional:** previous Alarm Details can be accessed via <code>metadata.prevAlarmDetails</code>. 
If previous Alarm does not exist, this field will not be present in Metadata. **Note** that  <code>metadata.prevAlarmDetails</code> 
is a raw String field and it needs to be converted into object using this construction:
{% highlight javascript %}
var details = {};
if (metadata.prevAlarmDetails) {
    details = JSON.parse(metadata.prevAlarmDetails);
}
{% endhighlight %}


**Alarm Details Builder** script function can be verified using [Test JavaScript function](/docs/{{docsPrefix}}user-guide/rule-engine-2-0/overview/#test-script-functions).
 
**Example of Details Builder Function**

This function takes <code>count</code> property from previous Alarm and increment it. Also put <code>temperature</code>
attribute from inbound Message payload into Alarm details.

{% highlight javascript %}
var details = {temperature: msg.temperature, count: 1};

if (metadata.prevAlarmDetails) {
    var prevDetails = JSON.parse(metadata.prevAlarmDetails);
    if(prevDetails.count) {
        details.count = prevDetails.count + 1;
    }
}

return details;
{% endhighlight %}


**Alarm created/updated with those properties:**

- Alarm details - object returned from **Alarm Details Builder** script
- Alarm status - if **new alarm** -> *ACTIVE_UNACK*. If **existing Alarm** -> does not changed
- Severity - value from Node Configuration
- Propagation - value from Node Configuration
- Alarm type - value from Node Configuration
- Alarm start time - if **new alarm** -> *current system time*. If **existing Alarm** -> does not changed
- Alarm end time - *current system time*

**Outbound message will have the following structure:**

- **Message Type** - *ALARM*
- **Originator** - the same originator from inbound Message
- **Payload** - JSON representation of new Alarm that was created/updated
- **Metadata** - all fields from original Message Metadata  

After new Alarm **_created_**, Outbound message will contain additional property inside Metadata - **isNewAlarm** with **true** value.
Message will be passed via **Created** chain.

After existing Alarm **_updated_**, Outbound message will contain additional property inside Metadata - **isExistingAlarm** with **true** value.
Message will be passed via **Updated** chain.

Here is an example of Outbound Message **payload**
{% highlight json %}
{
  "tenantId": {
    "entityType": "TENANT",
    "id": "22cd8888-5dac-11e8-bbab-ad47060c9bbb"
  },
  "type": "High Temperature Alarm",
  "originator": {
    "entityType": "DEVICE",
    "id": "11cd8777-5dac-11e8-bbab-ad55560c9ccc"
  },
  "severity": "CRITICAL",
  "status": "ACTIVE_UNACK",
  "startTs": 1526985698000,
  "endTs": 1526985698000,
  "ackTs": 0,
  "clearTs": 0,
  "details": {
    "temperature": 70,
    "ts": 1526985696000
  },
  "propagate": true,
  "id": "33cd8999-5dac-11e8-bbab-ad47060c9431",
  "createdTime": 1526985698000,
  "name": "High Temperature Alarm"
}
{% endhighlight %}

More details about Alarms in the Thingsboard can be found in [this tutorial](/docs/{{docsPrefix}}user-guide/alarms/)

You can see the real life example, where this node is used, in the next tutorial:

- [Create and Clear Alarms](/docs/user-guide/rule-engine-2-0/tutorials/create-clear-alarms/)

<br>

## Clear Alarm Node

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-clear-alarm.png)

This Node loads the latest Alarm with configured **Alarm Type** for Message Originator and Clear the Alarm if it exist.

Node Configuration:

- **Alarm Details Builder** script
- **Alarm Type** - any string that represents Alarm Type

Note: Since TB Version 2.3.0 the rule node has the ability to get alarm type using pattern with fields from message metadata:

   ![image](/images/user-guide/rule-engine-2-0/nodes/action-clear-alarm-fetch-alarm-type-from-metadata.png)

**Alarm Details Builder** script used for updating Alarm Details JsonNode. It is useful for storing additional parameters
inside Alarm. For example you can save attribute name/value pair from Original Message payload or Metadata.

**Alarm Details Builder** script should return **details** object. 

![image](/images/user-guide/rule-engine-2-0/nodes/action-clear-alarm-config.png)
 
- Message _payload_ can be accessed via <code>msg</code> property. For example <code>msg.temperature</code><br> 
- Message _metadata_ can be accessed via <code>metadata</code> property. For example <code>metadata.customerName</code><br> 
- Message _type_ can be accessed via <code>msgType</code> property. For example <code>msgType</code><br>
- Current Alarm Details can be accessed via <code>metadata.prevAlarmDetails</code>. 

**Note** that  <code>metadata.prevAlarmDetails</code> 
is a raw String field and it needs to be converted into object using this construction:
{% highlight javascript %}
var details = {};
if (metadata.prevAlarmDetails) {
    details = JSON.parse(metadata.prevAlarmDetails);
}
{% endhighlight %}

**Alarm Details Builder** script function can be verified using [Test JavaScript function](/docs/{{docsPrefix}}user-guide/rule-engine-2-0/overview/#test-script-functions).

**Example of Details Builder Function**

This function takes <code>count</code> property from previous Alarm and increment it. Also put <code>temperature</code>
attribute from inbound Message payload into Alarm details.
{% highlight javascript %}
var details = {temperature: msg.temperature, count: 1};

if (metadata.prevAlarmDetails) {
    var prevDetails = JSON.parse(metadata.prevAlarmDetails);
    if(prevDetails.count) {
        details.count = prevDetails.count + 1;
    }
}

return details;
{% endhighlight %}

 
This Node updates Current Alarm:

- change alarm **status** to **CLEARED_ACK** if it was already acknowledged, otherwise to **CLEARED_UNACK**
- set **clear time** to current system time
- update Alarm details with new object returned from **Alarm Details Builder** script


In case when Alarm does not exist or it is already **Cleared** Alarm, original Message will be passed to the next nodes via **False** chain.

Otherwise new Message will be passed via **Cleared** chain.

**Outbound message will have the following structure:**

- **Message Type** - *ALARM*
- **Originator** - the same originator from inbound Message
- **Payload** - JSON representation of Alarm that was cleared
- **Metadata** - all fields from original Message Metadata. Also additional property inside Metadata will be added -> **isClearedAlarm** with **true** value.

Here is an example of Outbound Message **payload**
{% highlight json %}
{
  "tenantId": {
    "entityType": "TENANT",
    "id": "22cd8888-5dac-11e8-bbab-ad47060c9bbb"
  },
  "type": "High Temperature Alarm",
  "originator": {
    "entityType": "DEVICE",
    "id": "11cd8777-5dac-11e8-bbab-ad55560c9ccc"
  },
  "severity": "CRITICAL",
  "status": "CLEARED_UNACK",
  "startTs": 1526985698000,
  "endTs": 1526985698000,
  "ackTs": 0,
  "clearTs": 1526985712000,
  "details": {
    "temperature": 70,
    "ts": 1526985696000
  },
  "propagate": true,
  "id": "33cd8999-5dac-11e8-bbab-ad47060c9431",
  "createdTime": 1526985698000,
  "name": "High Temperature Alarm"
}
{% endhighlight %}


More details about Alarms in the Thingsboard can be found in [this tutorial](/docs/{{docsPrefix}}user-guide/alarms/)

You can see the real life example, where this node is used, in the next tutorial:

- [Create and Clear Alarms](/docs/user-guide/rule-engine-2-0/tutorials/create-clear-alarms/)

<br>

## delay (deprecated)

Delays incoming messages for a configurable period. In other words, node receives a message, holds it for a set duration, and then sends it to the next rule nodes for further action.

**Configuration**

![Configuration example image](/images/user-guide/rule-engine-2-0/nodes/action-delay-config.png)

* **Period value** - number that tells the node how long to delay. For example, if you put 5 here, it means you want the node to wait for 5 units of time.
* **Period time unit** - time unit you're using for the delaying period. Available values are: seconds, minutes, hours. So, when paired with the **Period value**, if you chose 5 for **Period Value** and seconds for **Period time unit**, the node would wait for 5 seconds.
* **Maximum pending messages** - limit on how many messages the node can delay at once. For example, If you set a number like 1000, it means the node can delay up to 1000 messages at a time. Once this limit is reached, any new incoming messages will be routed via **Failure** connection type until there's space available.

> **Note:** **Period value** and **Period time unit** fields support templatization.

**Output connections**
* **Success:**
  * If message was delayed successfully.
* **Failure:** 
  * If maximum pending messages is reached.
  * If unexpected error happened during messages processing.

> **Note:** Incoming messages are not modified during processing.

**Usage example: waiting for external long-running tasks**

Consider the following scenario: we have an external API that initiates a long-running task. Upon the initial request, the API responds immediately, indicating that the task has started. However, we need to ensure the task is completed before we can proceed with further processing.

Solution with delay node:
1. **Initiate the task**: Our rule chain starts with the REST API call node, which makes a request to the external API to initiate the long-running task.
2. **Receive immediate response**: The external API quickly returns a response, confirming the task has been launched.
3. **Waiting for completion**: After receiving the initial response, instead of proceeding immediately, we introduce the delay node into our rule chain. This node is configured to introduce a 30-second wait, providing time for the external task to complete.
4. **Continue processing**: Once the delay is over, processing resumes, possibly involving another REST API call to check the status or retrieve results of the long-running task, and then proceeding with the next steps in the rule chain based on the task's completion status.

By using the delay node in this manner, we handle scenarios where immediate processing is not feasible due to external dependencies, ensuring smoother and more accurate message handling.

![Rule chain example image](/images/user-guide/rule-engine-2-0/nodes/action-delay-chain.png)

**Deprecation**

Because this node temporarily stores delayed messages in memory (thus, while message is in processing it is not persistent), they may be lost if ThingsBoard is restarted or node configuration is changed: these actions trigger node initialization during which old node state (which holds currently delayed messages) is cleared and new empty one is created.

> **Note:** If a sequential processing strategy is used, please, be aware that this node acknowledges incoming message, which will trigger processing of the next message in the queue.

## Generator Node

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-generator.png)

Generates Messages with configurable period. JavaScript function is used for message generation.

Node Configuration:

- Message generation frequency in seconds
- Message originator 
- JavaScript function that will generate the actual message.

JavaScript function receive 3 input parameters: 

- <code>prevMsg</code> - is a previously generated Message payload.
- <code>prevMetadata</code> - is a previously generated Message metadata.
- <code>prevMsgType</code> - is a previously generated Message type.

Script should return the following structure:
{% highlight java %}
{   
    msg: new payload,
    metadata: new metadata,
    msgType: new msgType 
}
{% endhighlight %}

![image](/images/user-guide/rule-engine-2-0/nodes/action-generator-config.png)

All fields in resulting object are optional and will be taken from previously generated Message if not specified.

Outbound Message from this Node will be new Message that was constructed using configured JavaScript function.

JavaScript generator function can be verified using [Test JavaScript function](/docs/{{docsPrefix}}user-guide/rule-engine-2-0/overview/#test-script-functions).

This node can be used for Rule Chain debugging purposes.

<br>

## Log Node 

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-log.png)

Transform incoming Message with configured JavaScript function to String and log final value into the Thingsboard log file. 

**INFO** log level is used for logging.

JavaScript function receive 3 input parameters 

- <code>metadata</code> - is a Message metadata.
- <code>msg</code> - is a Message payload.
- <code>msgType</code> - is a Message type.

Script should return String value.

![image](/images/user-guide/rule-engine-2-0/nodes/action-log-config.png)

JavaScript transform function can be verified using [Test JavaScript function](/docs/{{docsPrefix}}user-guide/rule-engine-2-0/overview/#test-script-functions).

You can see the real life example, where this node is used, in the next tutorial:

- [Reply to RPC Calls](/docs/user-guide/rule-engine-2-0/tutorials/rpc-reply-tutorial#log-unknown-request)

## RPC Call Reply Node

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-rpc-call-reply.png)

Sends response to the RPC Call originator. All incoming RPC requests are passed through Rule Chain as Messages.
Also all RPC requests have request ID field. It is used for mapping requests and responses.
Message Originator must be a **Device** entity because RPC response is initiated to the Message Originator.

Node configuration has special request ID field mapping. If the mapping is not specified, **requestId** metadata field is used by default. 

![image](/images/user-guide/rule-engine-2-0/nodes/action-rpc-call-reply-config.png)

RPC request can be received via different transports:

- MQTT
- HTTP
- CoAP  

Message payload example:
{% highlight json %}
{
  "method": "setGpio",
  "params": {
    "pin": "23",
    "value": 1
  }
}
{% endhighlight %}

Message will be routed via **Failure** chain in the following cases:

- Inbound Message originator is not a **Device** entity
- Request id is not present in the Message metadata
- Inbound Message payload is empty

For more details how RPC works in the Thingsboard, please read [RPC capabilities](/docs/{{docsPrefix}}user-guide/rpc/) Article.

You can see the real life example, where this node is used, in the next tutorial:

- [Reply to RPC Calls](/docs/user-guide/rule-engine-2-0/tutorials/rpc-reply-tutorial)

## RPC Call Request Node

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-rpc-call-request.png)

Sends RPC requests to the Device and routing response to the next Rule nodes.
Message Originator must be a **Device** entity as RPC request can be initiated only to device.

Node configuration has **Timeout** field used to specify timeout waiting for response from device.

![image](/images/user-guide/rule-engine-2-0/nodes/action-rpc-call-request-config.png)

Message payload must have correct format for RPC request. It must contains **method** and **params** fields.
Example:

{% highlight json %}
{
  "method": "setGpio",
  "params": {
    "pin": "23",
    "value": 1
  }
}
{% endhighlight %}

If Message Payload contains **requestId** field, its value used to identify RPC request to the Device. 
Otherwise random requestId will be generated.

Outbound Message will have same originator and metadata as in inbound Message. Response from the Device will be added into Message payload.

Message will be routed via **Failure** chain in the following cases:

- Inbound Message originator is not a **Device** entity
- Inbound Message has missed **method** or **params** fields
- If Node will not receive a response during configured timeout
 
Otherwise Message will be routed via **Success** chain.

For more details how RPC works in the Thingsboard, please read [RPC capabilities](/docs/{{docsPrefix}}user-guide/rpc/) article.

<br>

## save attributes {#save-attributes-node}

Stores message originator attributes from the incoming message based on configurable scope parameter.

**Configuration: general**

* **Attributes scope** - scope of the attributes where the attributes should be saved. Can be **_Client attributes_**, **_Server attributes_** or **_Shared attributes_**.
* **Attributes scope value** - value of the attributes scope that can be used in the message metadata to specify scope.
> **Note:** Use the 'scope' metadata key to dynamically set the attribute scope per message. You can copy value of **Attributes scope value** by simply clicking on the icon and use it as a value for key 'scope'. If provided, this overrides the scope set in the configuration.

**Configuration: advanced settings**

* **Save attributes only if the value changes** - if enabled, the rule node will remove current relations from the incoming message originator based on direction and type.
* **Send attributes updated notification** - if enabled, the rule node will change the message originator to related entity. Useful when you need to process submitted message as a message from target entity.

![Configuration example image](/images/user-guide/rule-engine-2-0/nodes/action-save-attributes-node-configuration.png)

Supported scope types:

- Client attributes
- Shared attributes
- Server attributes

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-attributes-config.png)

Expects messages with **POST_ATTRIBUTES_REQUEST** message type.
If message Type is not **POST_ATTRIBUTES_REQUEST**, Message will be routed via **Failure** chain. 

When attributes are uploaded over existing API (HTTP / MQTT / CoAP / etc.) Message with correct payload and type will be passed into **Input** node of the **Root Rule Chain**.

In cases when it is required to trigger attributes saving inside Rule Chain, the Rule Chain should be configured to transform Message payload 
to the expected format and set message type to **POST_ATTRIBUTES_REQUEST**. It could be done using [**Script Transformation Node**](/docs/{{docsPrefix}}user-guide/rule-engine-2-0/transformation-nodes/#script-transformation-node).

**Expected Message Payload example:**
{% highlight json %}
{
  "firmware_version": "1.0.1",
  "serial_number": "SN-001"
}
{% endhighlight %}

After successful attributes saving, original Message will be passed to the next nodes via **Success** chain, 
otherwise **Failure** chain is used.

<br>

## Save Timeseries Node 

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.0</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-timeseries.png)

Stores Timeseries data from incoming Message payload to the database and associate them to the Entity, that is identified by the Message Originator. 
Configured **TTL** seconds is used for timeseries data expiration. **0** value means that data will never expire.

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-timeseries-config.png)

Additionally, you could disable updating values for incoming keys for the latest timeseries data (ts_kv_latest table) if **'Skip latest persistence'** flag is set to **true**.
This could be helpful for highly loaded use-cases to decrease the pressure on the DB. 
Please note, this feature could be enabled when the use-case does not require advanced filtering on the Dashboards. 
For getting the latest value, the historical data could be fetched with limit 1 and DESC order.

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-timeseries-config-latest.png)

Expects messages with **POST_TELEMETRY_REQUEST** message type. 
If message Type is not **POST_TELEMETRY_REQUEST**, Message will be routed via **Failure** chain.
 
When timeseries data is published over existing API (HTTP / MQTT / CoAP / etc.) Message with correct payload and type will be passed into **Input** node of the **Root Rule Chain**.

In cases when it is required to trigger timeseries data saving inside Rule Chain, the Rule Chain should be configured to transform Message payload  
to the expected format and set message type to **POST_TELEMETRY_REQUEST**. It could be done using [**Script Transformation Node**](/docs/{{docsPrefix}}user-guide/rule-engine-2-0/transformation-nodes/#script-transformation-node).

Message Metadata must contain **ts** field. This field identifies timestamp in milliseconds of published telemetry.

Also, if Message Metadata contains **TTL** field, its value is used for timeseries data expiration, otherwise **TTL** 
from Node Configuration is used.

**Since TB Version 3.3.3** you can enable 'useServerTs' param to use the timestamp of the message processing instead of the timestamp from the message. 
Useful for all sorts of sequential processing if you merge messages from multiple sources (devices, assets, etc).

In the case of sequential processing, the platform guarantees that the messages are processed in the order of their submission to the queue. 
However, the timestamp of the messages originated by multiple devices/servers may be unsynchronized long before they are pushed to the queue. 
The DB layer has certain optimizations to ignore the updates of the "attributes" and "latest values" tables if the new record has a timestamp that is older than the previous record. 

So, to make sure that all the messages will be processed correctly, one should enable this parameter for sequential message processing scenarios.


**Expected Message Payload example:**
{% highlight json %}
{  
  "values": {
    "key1": "value1",
    "key2": "value2"
  }
}
{% endhighlight %}

After successful timeseries data saving, original Message will be passed to the next nodes via **Success** chain, 
otherwise **Failure** chain is used.

<br>

## Save to Custom Table

<table  style="width:250px;">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.3.1</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-to-custom-cassandra-table.png)

Node stores data from incoming Message payload to the Cassandra database into the predefined custom table that should have **cs_tb_** prefix, to avoid the data insertion to the common TB tables.

Please note, that rule node can be used only for **Cassandra DB**.

Configuration:

Administrator should set the custom table name without prefix: **cs_tb_**.

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-to-custom-cassandra-table-name-config.png)

Administrator can configure the mapping between the Message field names and Table columns name. If the mapping key is **$entityId**, that is identified by the Message Originator, then to the appropriate column name(mapping value) will be write the message originator id.

![image](/images/user-guide/rule-engine-2-0/nodes/action-save-to-custom-cassandra-table-config.png)

If specified message field does not exist in the **data** of the message or is not a JSON Primitive, the outbound message will be routed via **Failure** chain, otherwise, the message will be routed via **Success** chain.

**NOTE**: Please make sure that you are not using **metadata** keys in the configuration - only **data** keys are possible.  

<br>

## assign to customer {#assign-to-customer-node}

Identifies target customer by title and assigns message originator entity to this [customer](/docs/{{docsPrefix}}user-guide/ui/customers/).

> **Note:** Following message originator's entity types are supported: **Asset**, **Device**, **Entity View**, **Dashboard**, **Edge**.

**Configuration**

* **Customer title** - title to identify the target customer.
  > **Note:** Customer title field supports [templatization](/docs/{{docsPrefix}}user-guide/templatization/).
* **Create new customer if not exists** - if enabled, the rule node will create a new customer and assign message originator entity to it.

![Configuration example image](/images/user-guide/rule-engine-2-0/nodes/action-assign-to-customer-node-configuration.png)

**Output connections**
* **Success:**
  * If message originator entity was successfully assigned to a customer.
* **Failure:**
  * If message originator's entity type is unsupported.
  * If **Create new customer if not exists** is disabled and a customer by title does not exist.
  * If unexpected error occurs during message processing.

**Usage example**

Consider a smart building management system where various devices like thermostats, smoke detectors, and door sensors belong to different departments (customers) within a large office building.

For this case, we will use the configuration provided earlier.

We have a device, "SmokeDetector_101", that reports smoke level data. The device is located in a newly established department, "Marketing", which currently has no registered customer in the system.

![Device before image](/images/user-guide/rule-engine-2-0/nodes/action-assign-to-customer-example-device-before.png)

The incoming message from the device "SmokeDetector_101" will be as follows:

```bash
msg: {"smokeLevel": 0.04}, metadata: {"ts": "1616510426300", "departmentName": "Marketing"}
```

Since **Create new customer if not exists** is enabled, the rule node will fetch the customer's title from the message metadata, create a new customer with title "Marketing" and assign "SmokeDetector_101" to it.

![Device after image](/images/user-guide/rule-engine-2-0/nodes/action-assign-to-customer-example-device-after.png)

## unassign from customer {#unnassign-from-customer-node}

Identifies target customer by title and unassigns message originator entity from this [customer](/docs/{{docsPrefix}}user-guide/ui/customers/).

> **Note:** Following message originator's entity types are supported: **Asset**, **Device**, **Entity View**, **Dashboard**, **Edge**.

**Configuration**

* **Unassign from specific customer if originator is dashboard** - if enabled and message originator is a **Dashboard**, the rule node will unassign message originator entity from a particular customer.
  > **Note:** The configuration to specify particular customer appears only if **Unassign from specific customer if originator is dashboard** is enabled.
  * **Customer title** - title to identify the target customer.
    > **Note:** Customer title field supports [templatization](/docs/{{docsPrefix}}user-guide/templatization/).

![Configuration example image](/images/user-guide/rule-engine-2-0/nodes/action-unassign-from-customer-node-configuration.png)

**Output connections**
* **Success:**
  * If message originator entity was successfully unassigned from a customer.
  * If message originator entity was not assigned to any customer.
* **Failure:**
  * If message originator's entity type is unsupported.
  * If message originator is a **Dashboard** and **Customer title** is not specified.
  * If message originator is a **Dashboard** and customer by title does not exist.
  * If unexpected error occurs during message processing.

**Usage example**

Consider a central monitoring system where a single dashboard is used to provide a unified view of various metrics across multiple departments in a large company. 
This common dashboard is used by different departments for general monitoring but needs to be restricted for specific departments.

For this case, we will use the configuration provided earlier.

We have a dashboard, "KPIs_Dashboard_Main", which displays key performance indicators (KPIs) such as system uptime, error rates, and network traffic. 
This dashboard is shared among several departments, including "Finance", "IT", and "HR".

![Dashboard before image](/images/user-guide/rule-engine-2-0/nodes/action-unassign-from-customer-example-dashboard-before.png)

Now, we need to unassign the "KPIs_Dashboard_Main" from the "Finance" department as their monitoring needs have changed. 
The dashboard should still be available to the "IT" and "HR" departments.

The incoming message from the dashboard "KPIs_Dashboard_Main" will be as follows:

```bash
msg: {"uptime": 99.9, "errorRate": 0.02}, metadata: {"ts": "1616510426300", "departmentName": "Finance"}
```

Since **Unassign from specific customer if originator is dashboard** is enabled, the rule node will fetch the customer’s title from the message metadata, identify the "Finance" department and 
then unassign "KPIs_Dashboard_Main" from the "Finance" department, ensuring that the dashboard is no longer accessible to the "Finance" team while remaining available to the "IT" and "HR" departments.

![Dashboard after image](/images/user-guide/rule-engine-2-0/nodes/action-unassign-from-customer-example-dashboard-after.png)

## create relation {#create-relation-node}

Finds target entity and creates a [relation](/docs/{{docsPrefix}}user-guide/entities-and-relations/#relations). with the incoming message originator based on the configured direction and type.

**Configuration: Relation parameters**

* **Direction** - direction of the relation. Either **_From originator to target entity_** or **_From target entity to originator_**.
* **Relation type** - type of the relation. Default relation types are "Contains" and "Manages", but you may create relation of any type.

**Configuration: Target entity**

* **Type** - entity type of target entity. For each entity type some specific configurable input fields can appear, when specific entity type is selected:
  * **Asset** or **Device**:
    * **Device/Asset name** - name of the target entity.
    * **Profile name** - name of the target entity profile.
    > **Note:** All input fields support [templatization](/docs/{{docsPrefix}}user-guide/templatization/).
    * **Create new entity if it doesn't exist** - if enabled, a new entity with specified parameters will be created and used to create relation unless it already exists.
  * **Customer**:
    * **Customer title** - title of the target customer.
      > **Note:** **Customer title** field supports [templatization](/docs/{{docsPrefix}}user-guide/templatization/).
    * **Create new entity if it doesn't exist** - if enabled, a new customer with specified parameters will be created and used to create relation unless it already exists.
  * **Tenant**: there is no configurable input field. The current tenant will be used as a target entity.
  * **Entity View**, **User**, **Dashboard**, **Edge**:
    * **Entity view name/User email/Dashboard title/Edge name** - respectively, name/email/title of the target entity.

> **Note:** Following entity types are supported: **Tenant**, **Asset**, **Device**, **Customer**, **Entity View**, **Dashboard**, **Edge**, **User**.

**Configuration: advanced settings**

* **Remove current relations** - if enabled, the rule node will remove current relations from the incoming message originator based on direction and type.
* **Change originator to related entity** - if enabled, the rule node will change the message originator to related entity. Useful when you need to process submitted message as a message from target entity.

![Configuration example image](/images/user-guide/rule-engine-2-0/nodes/action-create-relation-node-configuration.png)

> **Note:** Following message originator's entity types are supported: **Tenant**, **Asset**, **Device**, **Customer**, **Entity View**, **Dashboard**, **Edge**, **User**.

**Output connections**
* **Success:**
  * If relation was successfully created.
* **Failure:**
  * If message originator is not supported.
  * If **Create new entity if it doesn't exist** for supported this property entities is disabled and the target entity type does not exist.
  * If unexpected error occurs during message processing.

**Usage example**

Consider a smart farming system where different devices are deployed across several fields to monitor soil moisture, temperature, and other conditions. 
Each device needs to be related to a specific field for accurate monitoring and reporting.

For this case, we will use the configuration provided earlier.

We have a device, "MoistureSensor_45", that monitors soil moisture levels in "Field_B". The system needs to establish a relationship between "MoistureSensor_45" and the asset representing "Field_B". 
If "Field_B" does not already exist in the system, it should be created automatically.

The incoming message from "MoistureSensor_45" will be as follows:

```bash
msg: {"moistureLevel": 35}, metadata: {"ts": "1616510426300", "fieldName": "Field_B", "fieldProfileName": "Field" }
```

Since **Create new customer if it does not exist** is enabled, the rule node will fetch the asset's name and asset profile's name from the message metadata, create new asset with the name "Field_B" and asset profile with the name "Field".

![Asset image](/images/user-guide/rule-engine-2-0/nodes/action-create-relation-example-asset.png)

A relation of type "Monitors" also will be created and established from "MoistureSensor_45" to "Field_B".

![Relation image](/images/user-guide/rule-engine-2-0/nodes/action-create-relation-example-relation.png)

And also message originator will be changed to "Field_B" asset.

## delete relation {#delete-relation-node}

Deletes the [relation](/docs/{{docsPrefix}}user-guide/entities-and-relations/#relations) from the selected entity to originator of the message by type and direction.

**Configuration: Relation parameters**

* **Direction** - direction of the relation. Either **_From originator_** or **_To originator_**.
* **Relation type** - type of the relation. Default relation types are "Contains" and "Manages", but you may create relation of any type.

**Configuration: other**

* **Delete relation with specific entity** - if enabled, the rule node will delete relation with just one particular entity. Otherwise, the relation will be rem oved with all matching entities.
  > **Note:** The configuration to specify particular entity appears only if **Delete relation with specific entity** is enabled.
  * **Type** - entity type of target entity. For each entity type some specific configurable input fields can appear, when specific entity type is selected:
  * **Asset**, **Device**, **Customer**, **Entity View**, **User**, **Dashboard**, **Edge**:
    * **Device name/Asset name/Customer title/Entity view name/User email/Dashboard title/Edge name** - respectively, name/title/email of the target entity.
      > **Note:** All input fields support [templatization](/docs/{{docsPrefix}}user-guide/templatization/).
  * **Tenant**: there is no configurable input field. The current tenant will be used as a specific entity.

> **Note:** Following entity types are supported: **Tenant**, **Asset**, **Device**, **Customer**, **Entity View**, **Dashboard**, **Edge**, **User**.

![Configuration example image](/images/user-guide/rule-engine-2-0/nodes/action-delete-relation-node-configuration.png)

> **Note:** Following message originator's entity types are supported: **Tenant**, **Asset**, **Device**, **Customer**, **Entity View**, **Dashboard**, **Edge**, **User**.

**Output connections**
* **Success:**
  * If relation was successfully deleted.
* **Failure:**
  * If message originator is not supported.
  * If **Delete relation with specific entity** is enabled and the target entity type does not exist.
  * If unexpected error occurs during message processing.

**Usage example**

Consider a fleet management system where multiple vehicles (devices) are related to different departments (assets). 
Over time, as the fleet or department structure changes, certain relationships may need to be removed.

For this case, we will use the configuration provided earlier.

We have a vehicle, "Truck_17", which was previously related to the "Logistics" department. 

![Device before image](/images/user-guide/rule-engine-2-0/nodes/action-delete-relation-device-before.png)

Now, this vehicle has been reassigned, and we need to delete the relation of type "Manages" between "Truck_17" and the "Logistics" department.

The incoming message from the vehicle "Truck_17" will be as follows:

```bash
msg: {"speed": 70, "location": "52.5200N, 13.4050E"}, metadata: {"ts": "1616510426300", "departmentName": "Logistics"}
```

The rule node will fetch the asset's name from the message metadata and delete configured relation between device with the name "Truck_17" and asset with the name "Logistics".

![Device after image](/images/user-guide/rule-engine-2-0/nodes/action-delete-relation-device-after.png)

## GPS Geofencing Events Node

<table  style="width:15%">
   <thead>
     <tr>
	 <td style="text-align: center"><strong><em>Since TB Version 2.3.1</em></strong></td>
     </tr>
   </thead>
</table> 

![image](/images/user-guide/rule-engine-2-0/nodes/action-gps-geofencing-event-node.png)

Produces incoming messages by GPS based parameters. Extracts latitude and longitude from incoming message data or metadata and returns different events based on configuration parameters (geo fence).

![image](/images/user-guide/rule-engine-2-0/nodes/filter-gps-geofencing-default-config.png)

The rule node fetches perimeter information from message metadata by default. If **Fetch perimeter information from message metadata** is unchecked, additional information should be configured.

<br>

###### Fetch perimeter information from message metadata

There are two options of area definition based on the perimeter type: **Polygon** and **Circle**

Metadata of the incoming message must include key with name **perimeter** and following data structure:

- Polygon

{% highlight java %}[[latitude1,longitude1],[latitude2,longitude2], ... ,[latitudeN,longitudeN]]{% endhighlight %}

- Circle

{% highlight java %}
{"latitude":"value1","longitude":"value2","radius":"value3","radiusUnit":"KILOMETER"}
{% endhighlight %}

Keys **"latitude"** and **"longitude"** it's coordinates of the point.

The **"radius"** key - it's the distance from the coordinate point to the circle.

All values for these keys are in double-precision floating-point data type.

The **"radiusUnit"** key requires specific value from a list of **METER**, **KILOMETER**, **FOOT**, **MILE**, **NAUTICAL_MILE** (capital letters obligatory).

###### Fetch perimeter information from node configuration
 
There are two options of area definition based on the perimeter type:
 
- Polygon 
             
![image](/images/user-guide/rule-engine-2-0/nodes/filter-gps-geofencing-polygon-config.png)           

- Circle
                  
![image](/images/user-guide/rule-engine-2-0/nodes/filter-gps-geofencing-circle-config.png)       

###### Event Types
There are 4 types of events managed by geofencing rule node:

- **Entered** — is reporting whenever latitude and longitude from the incoming message to belong the required perimeter area for the first time;
- **Left** — is reporting whenever latitude and longitude from the incoming message not belong the required perimeter area for the first time;
- **Inside** and **Outside** events are used to report current status.

Administrator can configure duration time threshold for reporting inside or outside event. For example, whenever minimal inside time is set to 1 minute the message originator is considered as being inside the perimeter 60 seconds after entering the area.
Minimal outside time defines whenever message originator is considered as out of the perimeter as well.

![image](/images/user-guide/rule-engine-2-0/nodes/action-gps-geofencing-event-node-duration-config.png)  
 
**Failure** chain will to be used when:

   - incoming message has no configured latitude or longitude key in data or metadata. 
   - missing perimeter definition;     

{% include templates/edge/edge-nodes.md %}

## copy to view

Copies attributes from the message originator to [entity view](/docs/{{docsPrefix}}user-guide/entity-views/) and changes message originator to related entity view.

> **Note:** Supported message types: **_Post attributes_**, **_Attributes Updated_**, **_Attributes Deleted_**, **_Activity Event_**, **_Inactivity Event_**.

**Output connections**
* **Success:**
  * If message originator entity's attributes was successfully copied to an entity view and message originator changed to the related entity view.
* **Failure:**
  * If message type is unsupported.
  * If message metadata is empty.
  * If unexpected error occurs during message processing.

**Usage example**

Consider a smart agricultural system where sensors in different fields monitor various attributes such as sensor status and operational parameters. 
The system uses entity views to provide tailored access to specific attributes for different agricultural teams, ensuring that each team only sees the relevant information for their assigned fields.

We have a device, "SoilSensor_202", that tracks attributes like `sensorStatus`, `lastCalibration` and `inactivityAlarmTime`.

![Device image](/images/user-guide/rule-engine-2-0/nodes/action-copy-to-view-example-device.png)

We also have an entity view, "FieldView_South", which is set up to provide access to these specific attributes to the "Irrigation" team, while excluding other irrelevant attributes like inactivityAlarmTime.

![Entity view before image](/images/user-guide/rule-engine-2-0/nodes/action-copy-to-view-example-entity-view-before.png)

The incoming message with the message type **_Attributes Updated_** from the device "SoilSensor_202" will be as follows:

```bash
msg: {"sensorStatus": "active", "lastCalibration": 1653020504700, "inactivityAlarmTime": 1723908190991}, metadata: {"ts": "1616510426300", "scope": "SERVER_SCOPE"}
```

The rule node will copy the updated attributes (sensorStatus and lastCalibration) from "SoilSensor_202" to the "FieldView_South" entity view 
and will change message originator to the "FieldView_South" entity view.

![Entity view after image](/images/user-guide/rule-engine-2-0/nodes/action-copy-to-view-example-entity-view-after.png)

You can see usage example of this rule node in the rule chain [here](/docs/{{docsPrefix}}user-guide/entity-views/#attributes-view).
