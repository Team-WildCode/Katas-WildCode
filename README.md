# WildLife.AI

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

# Sequence diagrams
- [Authentication and Authorization](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD%20-%20Authentication%20and%20Authorization.png)
- [GBIF Repository upload](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-%20GBIF.png)
- [Third party analysis](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-%20Third%20party%20analysis.png)
- [Camera control functionality](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/SQD-Camera%20Control.png)
- [Camera alert functionality](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/cameraAlert.png)
- [iNaturralist uploads](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/iNaturalist.png)
- [Model Ingestion to Camera funtionality](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/Model%20Ingestion%20to%20Camera.png)
- [Metadata Prediction and Sharing](https://github.com/Team-WildCode/Katas-WildCode/blob/main/Sequence%20Diagram/Metadata%20Prediction%20and%20Sharing.png)

# Architectural Characteristics

1. Scalability: The overall architecture We proposed with AI is designed to be scalable to meet the growing needs of wildlife conservation efforts. The architecture is designed to handle increasing data volumes and user demand, ensuring that it can effectively support conservation efforts across a wide range of scales.
 
2. Flexibility: The camera's software and hardware components are designed to be adaptable, allowing for customization and integration with various sensors, communication technologies((Lorawan, 3G, Satellite)), preferred third-party integrations  and external devices allow for easy deployment in diverse environments, from remote wilderness areas to densely populated regions i.e the open-source nature of the proposed solution enables customization and adaptation to specific conservation needs. Users can modify the camera's configuration, train species identification models for local wildlife, adding local CPUs RPI and AWS Snowcone and integrate the camera with existing conservation data management systems.
 
3. Security: The camera employs robust security protocols, encryption techniques and access controls, to protect sensitive data and prevent unauthorized access, ensuring the integrity of conservation efforts and protecting both wildlife and user information.
 
4. Fault Tolerance: The camera's hardware and software incorporates fault tolerance mechanisms within the firmware to minimize downtime and ensure continuous operation, data continuity even in challenging environments.
 
5. Usability: The camera interface are designed to be intuitive and user-friendly, making it easy for biologists and nature enthusiasts with all levels of technical expertise to operate and manage the camera, training models and uploading training models effectively.
 
6. Supportability: We are committed to providing comprehensive customer support including documentation, tutorials, and community forums and software updates, ensuring that users have the resources they need to maximize the camera's capabilities. A dedicated support team will address user queries, resolve technical issues, and release regular software updates to enhance functionality and security by taking user feedback.
 
7. Reliability:The components collectively empower users to effortlessly deploy, manage, and extract valuable insights from the wildlife cameras, thereby streamlining conservation efforts on a global scale.
 
8. Extensibility: The architecture is designed to accommodate future advancements in AI technology,edge computing and support the integration of new features and functionalities without disrupting the existing system architecture.
 
9. User-Centric Design: The mobile application is engineered for resilience and user-friendliness, the user can perfom various required opreartions which helps minimize user burden and maximize accessibility.
 
10. Cost-effective: Users can also use their hardware either RPI, AWS Snowcone based on their requirements and bugets.
 
11. Community-Driven Innovation: Developers and researchers, biologists and nature enthusiasts can contribute to the product's evolution by creating new features, optimizing models, and expanding communication protocols. This community-driven approach will accelerate advancements in AI-powered wildlife conservation.




 
