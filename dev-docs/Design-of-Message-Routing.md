# Hierarchical BPMN Message Routing against Diverse Scenarios
> Here we discuss the message routing spanning the third-party systems and  the process engine of the host system

### Message example
- Messages is derived from third-party systems which are accepted by process engines.Here are two examples.Here are two examples, one for temperature - messages and one for delay messages.
- Temperature messages :
  - <`Topic`: "/temperature" ,`Order`: "cooling" , `Input`: 10℃ >
- Delay messages :
  - < `Topic` : "/telay" , `Order`: "postpone"，`Input` ：1h >

 From the example we can see that we ues \<Topic,Order\> to carrythe message.Topic-parameter means which tpye of process should receive the message while Order-parameter means which order that is selected from command library the process contains the process should execute and the Input-parameter is parameters the order needs.  
### Event Gateway at the process engine level
>When process engine receive a messages it will resolve the Topic-parameter of message at first.Assume the Topic-parameter is Temperature ,then Event Gateway will send the messages to Message Exchange that belong to Temperature(cold-chain) field.
### Message Exchange at the process definition level
>When messages pass the Event Gateway Message Exchange will handle it.Different Message Exchange contains command library of different field.Message Exchange will resolve Order-parameter to select the corresponding order in command library,and then use the Input-parameter
to be parameters of the order.<br>
>All process instances belong to the field will receive the order.Every process instance maintain a Message Collection which contains message type that the process instance interest in.If a process instance is interested in the message, it will execute the order.
### Message Collection of Interest at the process instance level
>Every process instance maintain a Message Collection which contains message type that the process instance interest in.<br>
### Messaging schematic
<img src="https://www.processon.com/view/link/5be3d30fe4b0993bf7213010"/>  
