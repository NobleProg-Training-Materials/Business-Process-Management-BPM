# Business-Process-Management-BPM
## Categories
- SOA (Service-Oriented Architecture)
- BPM (Business Process Management)

## SOA Overview

- In SOA, services are typically parts of one or more distributed business processes.
- Main motivations for services come from business processes.

## BPM vs BPM

- **Business process management** usually refers to a technology-enabled means for companies to gain visibility and control over long-lived, multistep processes that span a wide range of systems and people in one or more organizations.
- **Business process modeling** is a set of practices or tasks that companies can perform to visually depict or describe all the aspects of a business process, including its flow, control and decision points, triggers and conditions for activity execution, the context in which an activity runs, and associated resources.

## BPM vs Workflow

- A business process describes **what** has to be done (including input and output). It might include manual activities and might use any kinds of resources.
- A workflow describes **how** a certain result can be reached. It looks further into the details of all the steps or activities.

## Discovering BPM Services

- **Top-down** approach: decompose a problem, system, or process into smaller chunks until you reach the level of (basic) services.
- **Bottom-up** approach: build business processes by composing services into more general chunks.
- Agile, middle-ground approach.

## Business Process Modeling

A model is a representation of the process that allows companies to document, simulate, share, implement, evaluate, and continually improve their operations.

## Using Business Process Modeling Tools

- Intalio
- ProcessMaker
- Oracle BPA
- ActiveBPM
- Tibco
- jBPM

![SOA BPM Modeling](Soa-bpm-modeling.jpg)

## BPEL

- BPEL is an XML language for describing business flows and sequences, which in themselves are services.
- Usually generated from a tool (and BPMN).

![BPEL Diagram](Soa-bpel.png)

### BPEL Code Snippet

```xml
<invoke partnerLink="ncname" portType="qname" operation="ncname"
        inputVariable="ncname"? outputVariable="ncname"?
        standard-attributes>
   standard-elements
   ...
   <catch faultName="qname" faultVariable="ncname"?>*
      activity
   </catch>
   <catchAll>?
      activity
   </catchAll>
   ...
</invoke>
````

### BPEL Example

```xml
<?xml version="1.0"?>
<process name="changeAddress" ...>
  <variables>
    <variable messageType="..." name="...">
  </variables>
  <flow>
    <receive .../>    <!-- for this request (operation and input) -->
    <invoke .../>     <!-- call other service -->
    <assign .../>     <!-- map data -->
    <reply .../>      <!-- return data -->
  </flow>
</process>
```

### BPEL in Practice

* To compose and/or orchestrate services, you need services.
* BPEL can be considered a business process assembler.
* BPEL has error-handling support.
* Supports data mappings.

## Orchestration

![Orchestration](Soa-orchestration.png)

* There is one central controller that coordinates all the activities of the process.
* You can apply the composite pattern, which means that the whole composition itself can be used as a service.
* Think of an orchestra and a conductor.

## Choreography

![Choreography](Soa-choreography.png)

* Each party is responsible for one or more steps.
* Nobody controls the process as a whole, and it might even be the case that nobody knows about or understands the process as a whole.
* Similar to a roundabout.

## Orchestration vs Choreography

* Orchestration depends on the “conductor”; it might not scale well.
* Centralization in orchestration creates order and control.
* Choreography comes naturally and scales well, but there is no single entity responsible for the whole process.
* Choreography depends highly on collaboration and the specification of general rules to prevent chaos.

## Questions

* What does BPM stand for?
* What are the trade-offs in case of top-down and bottom-up approaches?
* What is BPEL?
* How do BPMN and BPEL relate?

## BPM resources

[BPM Training | NobleProg](https://www.nobleprog.cz/en/bpm-training)
