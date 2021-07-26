
## **Component**

### What is the component?

The proccess of dividing the design into **individual functional**or **logical components** to represent it in a good communication interface containing methods, events, and properties. 


### What are the advantages of using component based architecture?

1. Ease of deployment 

2. Reduced cost 

3. Ease of development 

4. Reusable 

5. Modification of technical complexity 

6. Reliability

7. System maintenance and evolution 

8. Independent 

### What are the charactistics of a component? 

**Path**. A location in the folder in which to store components. Use folders to organize components in a hierarchical manner.

**Component name**. The name of the component.

**Component type name**. The name of the component type that is associated with a component. 

The provisioning system includes some component types that support generic models, such as files and directories. Additional component types can be added to the system by importing plug-ins that are specific to application domains, such as Microsoft Windows and WebLogic.

**Version number**. The version number of the component. Each time a component is modified, the version number increments.

At check-in time, you choose how to increment the version number. You can increment by the major number, which is to the left of the decimal point, or by the minor number, which is to the right of the decimal point.

**Platform**. The operating system on which this component can be installed.

**Check-in date**. The date and time when the component was checked in.

**Check-in user**. The user ID of the person who checked in the component. This attribute is useful when you want to audit provisioning system processes.

**Label**. An optional string that you can use to categorize or group components.

**Category**. An optional object that you can use to filter the component list. After you create a category object, you can subsequently use it to group components.

**Description**. An optional string that describes the component. Use this attribute to provide meaningful information about the component.

**Source**. The resource that has been included in this component. The source can be a single file resource or a list of other components.

**Component variables**. A list of variables and their values (name-value pairs) that are required to deploy a component resource. 

**Procedures**. A set of instructions that specifies what to do with the resources and variables.

**Hidden**. A characteristic that indicates whether you can view the component in a list of components. By default, components are not hidden.

[**Source**](https://docs.oracle.com/cd/E19636-01/819-1659/componentcharacteristics/index.html) I used for the above question.


# **Props**

### What is props short for?

`Props is a special keyword in React, which stands for properties and is being used for passing data from one component to another.` Note that props are used in **uni-directional** flow. (from parent to child).

### How are props used in React?

The following steps simplifies the proccess of using props:

1. Firstly, define an attribute and its value(data).

2. Then pass it to child component(s) by using Props.

3. Finally, render the Props Data.

### What is the flow of props?

As we have mentioned before, it's uni-directional flow (from parent to child). In other words, `data coming from the parent should not be changed by child components.`