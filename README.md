
# Smart car management system

## Technical requirements

* set of separate (virtual) machines, with network isolation

* secure communication tunnel (e.g. TLS, SSH) using correct configuration

* design and deployment of one mechanism using a custom security protocol

## Project specific requirements

* network segmentation

* simulated Trusted Execution Environment (`TEE`)

* You may simulate each part of the system with a VM (including the `TEE`)
or a client application and use sockets to simulate the connections.

## Car system must include

### In the car

* A `Control Unit` server that manages all the car's systems and external communications

* The `TEE` of the `Control Unit` that handles and protects critical operations

* `Pedal peripherals`, directly connected to the `TEE` by a dedicated bus, that may trigger the accelerate and brake operations

* `Engine controller` connected to the `Control Unit` that validates accelerate operations and regulates the throttle

* `Brake controller` connected to the `Control Unit` that validates brake operations and brakes the wheels

### In the manufacturer

* A service that allows users to connect to their cars (with their phone or computer), to open doors, regulate the AC, and monitor tire pressure and fuel levels

#### The `TEE` VM may have

* prestored certificate

* prestored private key

* service that receives, validates and executes programs

* direct secure bus to the pedals (may be simulated with sockets)

* memory region shared with the main system (may also be simulated with sockets)

## Proposal

* proposal document must be submitted on that same week, on the day following the lab session

* should describe three versions of the work: basic, intermediate and advanced

* Mandatory file name `A47_Fri_14:00_13_proposal.pdf`

* Report cover: Project title. Headed by course name, group campus, group number. In the next row: group members sorted by ascending student number. For each student, include the number, name and professional photo;

* Report body: The font should be no smaller than 11pt, with standard line and character spacing;

* Limit 4 pages (excluding cover);

* Pages should be numbered (preferably with a label like Page X of Y);

* The use of diagrams (such as UML) is recommended for clear and concise communication.

### Document structure

Problem:
Given the chosen scenario, where is security necessary?
What is the main problem being solved?
Use around 200 words.

1.1. Requirements
Which security requirements were identified for the solution?
Present as a list.

1.2. Trust assumptions
Who will be fully trusted, partially trusted, or untrusted?
Write down the trust relationships to make them explicit.
Proposed solution

2.1. Overview
Diagram and explanation with at most 200 words.

2.2. Deployment
Describe distinct machines and how they will be interconnected.

2.3. Secure channel(s) to configure
Identify communication entities.
Choose existing TLS or SSH library/tool to use. What keys will exist and how will they be distributed.

2.4. Secure protocol(s) to develop
Who will communicate?
Identify communication entities and the messages they exchange with a sequence or collaboration diagram.
Identify the security properties to ensure.
Choose language for implementation.
What keys will exist and how will they be distributed?
Plan

3.1. Versions
Describe basic, intermediate and advanced versions of the work and when are they expected to be achieved.

3.2. Effort commitments
Table containing one row per week until the submission date and one column per group member with expected activities for the given week.
Some cells may be left blank because of work in other courses.
References
Tools, libraries, and other references that will be used in the project.

## Resources

* [Survey of the Connected Vehicles](https://ieeexplore.ieee.org/abstract/document/8058008)

* [Open-TEE](https://ieeexplore.ieee.org/document/7345308) (not for direct use, but for reference)

* [Project overview git](https://github.com/tecnico-sec/Project-Overview-2021_1)

* [Topics git](https://github.com/tecnico-sec/Project-Topics-2021_1/blob/main/README.md)
