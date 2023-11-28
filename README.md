# WildLife.AI

TABLE OF CONTENTS
=================
- [Prelude](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#prelude)
- [Vision](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#vision)
- [Business Requirements](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#business-requirements)
  - [Short term](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#short-term)
  - [Mid term](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#mid-term)
  - [Long term](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#long-term)
- [Strategy](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#strategy)
- [System Architecture](https://github.com/Team-WildCode/Katas-WildCode/blob/main/README.md#system-architecture)
  - [Core Components of System Architecture](https://github.com/Team-WildCode/Katas-WildCode/#core-components-of-system-architecture)
    - [User-Centric Mobile Application](https://github.com/Team-WildCode/Katas-WildCode/#user-centric-mobile-application)
    - [Metadata Sharing and Firmware Integration](https://github.com/Team-WildCode/Katas-WildCode/#metadata-sharing-and-firmware-integration)
    - [Adaptive Communication Models](https://github.com/Team-WildCode/Katas-WildCode/#adaptive-communication-models)
    - [Model Training and Repository](https://github.com/Team-WildCode/Katas-WildCode/#model-training-and-repository)
    - [Integration with Analysis Platforms](https://github.com/Team-WildCode/Katas-WildCode/#integration-with-analysis-platforms)
    - [User Feedback and Improvement Loop](https://github.com/Team-WildCode/Katas-WildCode/#user-feedback-and-improvement-loop)
 - [Architectural Characteristics](https://github.com/Team-WildCode/Katas-WildCode/#architectural-characteristics)
 - [Architecture Style](#long-term-expansions)
- [ADR's](https://github.com/Team-WildCode/Katas-WildCode/#adrs)
- [References](https://github.com/Team-WildCode/Katas-WildCode/#references)

# Prelude

All successful initiatives stories start with a problem to solve. Here is one very deep and crucial for the mankind -"Conservation of wildlife".The conservation of wildlife is indeed a crucial aspect of our ecosystem, with far-reaching implications for both the natural world and human society. Many species are on the brink of extinction or have already disappeared, largely due to habitat destruction, climate change, poaching, and various human activities. To counter this trend, wildlife conservation efforts have gained momentum globally, and the incorporation of technology, especially machine learning and AI, has significantly enhanced these initiatives.

One notable organization in this field is wildlife.ai, a non-profit organization that leverages technology to aid wildlife conservation.Initiatives like wildlife.ai, which combine technology and wildlife conservation, offer a promising approach to safeguarding the planet's natural heritage. By using remote cameras and AI, these initiatives provide valuable insights, promote informed decision-making, and contribute to the protection of both wildlife and the ecosystems on which human life depends. The preservation of wildlife is a shared responsibility and, should be undertaken with love and care.

Our goal as a team is to help wildlife.ai is to connect the dots, by creating a conservation ecosystem that can grow, expand, thrive and benefit both - the wildlife and researchers.

# Vision

Started with Weta-watcher to building open source wildlife camera is thriving journey. Unleashing the potential of Artifical Intelligence in wildlife is what wildlife.ai is aiming at. Educating community groups, students, publishing magazines , organizing events to educate people about wildlife conservation . Providing platform to build and train models for great initiative. This platform provides a way to engage ourselves based on the skill we have, be it nature enthusiast, biologist , ML engineer or a Student. With our contribution to this initiative we are just not providing archtiecture but also helping to save hundreds and thousands of species from extinction. 


# Business Requirements

# Short term 
- Development and support of core features of the camera.
- Monitor camera working under different scalable condition, until backend infrastructure stabilizes.
- Scale the architecture for more users.

# Mid term
- Launch camera with different specifications based supporting different features for different user groups.
- Scale for hundreds and thousands of people.
- Provide community sessions and discussion forums explaining usage of camera effectively.
- Integration of AWS Snowcone, Raspberry Pi, Waveshare and other relevant hardwares and softwares.
- Create a core learning and support team to teach community about building, training and sustaining machine learning models.

# Long term
- Support partnerships and donations.
- Offers wildlife conservation badge to users on successful species occurence, GBIF submission.
- Establish a platform for engagement between experts and community for knowledge sharing sessions about product and wildlife.
- Establish a social network around the motto of "Wildlife savers".


# Strategy

Modern technologies and Cloud enable rapid experimentation and development of distributed systems that were considered very complex several years ago. Within a few clicks or lines of code we can spin out a whole environment with databases, message brokers and microservices securely deployed in the Cloud of our choice. We can then gradually and continuously experiment our ideas, hypothesis and thus delight our customers with solving they toughest pains. Therefore, our strategy is to define initial architecture based on customer feedbacks as an ideal target state (which of course will evolve) and aim to to that. Here, we see no benefit in investing time and effort in creating technical debt and building monolithic systems or components which will (require refactoring and re-engineering in the future. Of course if we experiment with something that we don’t know we can do temporary trade-offs and simplifications, but we should have a very clear reason for NOT aiming to the ideal target state. Unless, we are building a minimum viable product for rapid experimentation with new hypothesis and we are not sure about future requirements, customer needs or market. Our main principle is that "we are not rich enough to buy cheap things".

# System Architecture

Our platform is designed to fulfill the requirements outlined by Wildlife AI, encompassing user management, camera operations, notification dispatch, multimedia processing such as images and videos, and collaboration with our associates and suppliers. For better structure, we've allocated each domain to a dedicated module in our proposed framework.

![Wildlife Component Diagram](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Wildlife%20Component%20Diagram.png)

## Core Components Of System Architecture

### User-Centric Mobile Application

Our proposed mobile app empowers users to effortlessly control cameras, modify settings, and update models without physically accessing the devices. Featuring individual and group registration, varying access levels, and a robust password reset module, the app ensures seamless management, with all data securely stored in a central database.

#### Camera Control

![SQD-Camera Control](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-Camera%20Control.png)

#### Authentication and Authorization

![SQD - Authentication and Authorization](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD%20-%20Authentication%20and%20Authorization.png)

### Notification Alerts and Metadata Sharing

The camera, equipped with sensors and an SD card for storage, captures footage and forwards it to the model. This firmware orchestrates communication with memory cards, external devices, and wireless connectivity options. 

Periodic heartbeat status updates and predicted metdata are sent to mobile application which enable error detection, ensuring efficient data transfer and analysis. Predicted species data is seamlessly relayed to users in real-time. It ensures efficient storage and management of captured images and videos, while also facilitating data transfer to other devices for in-depth analysis.

#### Model Ingestion To Camera

![Model Ingestion To Camera](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/Model%20Ingestion%20to%20Camera.png)

#### Metadata Prediction and Sharing

![Metadata Prediction and Sharing](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/Metadata%20Prediction%20and%20Sharing.png)

### Adaptive Communication Models

Diverse communication models—LoRaWAN(Places with no cellular network), 3G(Nearby forests, rural areas), Satellite(Sea, forests etc)—are employed based on geographical deployment, catering to various terrains and connectivity challenges. These models are integrated into a comprehensive network stack, ensuring seamless model execution in different environments.

#### Communication Models

![Communication Models](https://github.com/Team-WildCode/Katas-WildCode/blob/main/images/Communication%20Models.png)

### Model Training and Repository

Utilizing third-party services like Roboflow, Edge Impulse, or TensorFlow Lite, data preprocessing ,model training and species prediction occur. The AI model plays a pivotal role in identifying the species captured by the camera. It analyzes the footage and generates predictions with high accuracy, providing crucial insights for conservation efforts. The predictions, along with relevant metadata, are then transmitted to users via notification alerts.

Users can trigger model checkpoint files, stored in a trained model database, to be uploaded and executed on local CPUs (Raspberry Pi or AWS Snowcone) after predicting the new metadata. To accommodate a wide range of deployment scenarios, we offer two hardware variants for running the trained model: Raspberry Pi and AWS Snowcone. Users can select the most suitable option based on their budget and requirements, ensuring optimal performance and cost-effectiveness. The model repository serves as a central hub for storing all checkpoint files, providing a secure and organized environment for managing and accessing AI models.

#### Model Training Repository

![SQD- Model Training](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-%20Model%20training.png)

#### Camera Alert

![Camera Alert](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/cameraAlert.png)


### Integration with Analysis Platforms

Users gain access to common camera trap labeling platforms such as Wildlife Insights, TrapTagger, and Trapper, fostering video analysis and frame publication. Users can publish frames from the videos to iNaturalist, a renowned citizen science platform, to seek expert opinions on species identification and classification. This collaboration with experts enhances the accuracy of species identification and provides valuable insights for conservation decision-making.The architecture further enhances data utilization by enabling users to convert data to Cantrap DP data exchange format and publish species occurrences to the Global Biodiversity Information Facility (GBIF). This integration facilitates the exchange of critical biodiversity data with global conservation initiatives, amplifying the impact of individual conservation efforts.

#### Third Party Analysis

![SQD- Third Party Analysis](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-%20Third%20party%20analysis.png)

#### iNaturalist uploads

![iNaturralist](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/iNaturalist.png)

#### GBIF Uploads

![SQD- GBIF](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-%20GBIF.png)

### User Feedback and Improvement Loop

We prioritize user feedback by providing a dedicated service for customers to contribute suggestions and improvements. A dedicated user feedback service allows users to provide suggestions and report any issues. All feedback is stored in the user feedback repository for review and action.

## Architectural Characteristics

1. **Scalability**: The overall architecture We proposed with AI is designed to be scalable to meet the growing needs of wildlife conservation efforts. The architecture is designed to handle increasing data volumes and user demand, ensuring that it can effectively support conservation efforts across a wide range of scales.
 
2. **Flexibility**: The camera's software and hardware components are designed to be adaptable, allowing for customization and integration with various sensors, communication technologies((Lorawan, 3G, Satellite)), preferred third-party integrations  and external devices allow for easy deployment in diverse environments, from remote wilderness areas to densely populated regions i.e the open-source nature of the proposed solution enables customization and adaptation to specific conservation needs. Users can modify the camera's configuration, train species identification models for local wildlife, adding local CPUs RPI and AWS Snowcone and integrate the camera with existing conservation data management systems.
 
3. **Security**: The camera employs robust security protocols, encryption techniques and access controls, to protect sensitive data and prevent unauthorized access, ensuring the integrity of conservation efforts and protecting both wildlife and user information.
 
4. **Fault Tolerance**: The camera's hardware and software incorporates fault tolerance mechanisms within the firmware to minimize downtime and ensure continuous operation, data continuity even in challenging environments.
 
5. **Usability**: The camera interface are designed to be intuitive and user-friendly, making it easy for biologists and nature enthusiasts with all levels of technical expertise to operate and manage the camera, training models and uploading training models effectively.
 
6. **Supportability**: We are committed to providing comprehensive customer support including documentation, tutorials, and community forums and software updates, ensuring that users have the resources they need to maximize the camera's capabilities. A dedicated support team will address user queries, resolve technical issues, and release regular software updates to enhance functionality and security by taking user feedback.
 
7. **Reliability**:The components collectively empower users to effortlessly deploy, manage, and extract valuable insights from the wildlife cameras, thereby streamlining conservation efforts on a global scale.
 
8. **Extensibility**: The architecture is designed to accommodate future advancements in AI technology,edge computing and support the integration of new features and functionalities without disrupting the existing system architecture.
 
9. **User-Centric Design**: The mobile application is engineered for resilience and user-friendliness, the user can perfom various required opreartions which helps minimize user burden and maximize accessibility.
 
10. **Cost-effective**: Users can also use their hardware either RPI, AWS Snowcone based on their requirements and bugets.
 
11. **Community-Driven Innovation**: Developers and researchers, biologists and nature enthusiasts can contribute to the product's evolution by creating new features, optimizing models, and expanding communication protocols. This community-driven approach will accelerate advancements in AI-powered wildlife conservation.

## Architecture Style

The proposed solution utilizes a synergistic combination of microservices, service-oriented architecture (SOA), and event-driven architecture (EDA) to achieve the desired functionality and address the aforementioned challenges.

Microservices architecture is employed to compartmentalize the application into independent, fine-grained services, each responsible for a specific business capability. The services communicate seamlessly through well-defined APIs, promoting loose coupling and simplified development.

SOA principles are embedded to ensure interoperability between the disparate components, enabling seamless integration with existing systems.

EDA is leveraged to facilitate real-time communication among the microservices, enabling near-instantaneous responses to events and fulfilling the demand for responsive, dynamic behavior. The event-driven paradigm effectively addresses the constraints of uncertain environments by providing a resilient, asynchronous communication mechanism.

In essence, the proposed architecture harmonizes the strengths of microservices, SOA, and EDA to deliver a robust, scalable, and adaptable solution that meets the demands of near-real-time communication and responsiveness in uncertain environments.

![Architecture Worksheet](https://github.com/Team-WildCode/Katas-WildCode/blob/main/images/Architecture_Worksheet.png)

# ADRs

The below ADRs contains the architectural decisions regarding the proposed design including required context and rationale

[AD001](https://github.com/Team-WildCode/Katas-WildCode/blob/main/ADRs/AD001%20-%20MobileApplicationWithCameraInteraction.md) - A mobile application that allows customers to interact with a camera system

[AD002](https://github.com/Team-WildCode/Katas-WildCode/blob/main/ADRs/ADR002%20-%20ModelTrainingAndThirdPartyAnalysis.md) - Leveraging AI for species identification through camera traps can significantly enhance the speed and accuracy of data analysis.

[AD003](https://github.com/Team-WildCode/Katas-WildCode/blob/main/ADRs/ADR003%20-%20NotificationAlert.md) - Implementing a system that enables the camera to send periodic heartbeat status updates to the user via a mobile application and interact with the camera software to retrieve prediction metadata.

[AD004](https://github.com/Team-WildCode/Katas-WildCode/blob/main/ADRs/ADR004%20-%20UserFeedbackService.md) - Establish a dedicated User Feedback Service to facilitate seamless communication between users and the development team.

# Video Presentation

[WildCodeWranglers Presentation Video](https://github.com/Team-WildCode/Katas-WildCode/blob/main/WildCodeWranglers%20Presentation%20Video.mp4)

# References

1. [Communication Patterns](https://communicationpatternsbook.com/freebies.html)
2. [Software Architecture Patterns](https://www.oreilly.com/library/view/software-architecture-patterns/9781098134280/)
3. [Designing Machine Learning](https://learning.oreilly.com/library/view/designing-machine-learning/9781098107956/)
4. [Worksheets](https://www.developertoarchitect.com/resources.html)
