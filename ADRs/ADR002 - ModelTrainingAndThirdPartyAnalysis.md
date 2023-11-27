# Title: Model Training And Third Party Analysis

## Status:
Proposed

## Context:

**Challenge**: Conservation efforts often require efficient and accurate species identification, which can be challenging and time-consuming.

**Opportunity**: Leveraging AI for species identification through camera traps can significantly enhance the speed and accuracy of data analysis.

## Rationale:

1. **AI for Conservation**:
Integrating AI models enables automated species identification from camera trap footage, reducing manual effort and providing real-time insights.
2. **Flexible Deployment**:
Offering both Raspberry Pi and AWS Snowcone as hardware options allows users to choose based on their specific needs, considering factors like budget and computational requirements.
3. **Collaboration and Data Exchange**:
Integration with labeling platforms, citizen science initiatives, and global biodiversity data exchange platforms enhances the collaborative nature of conservation efforts.

## Decision:

1. **Third-Party Services**:
Selection of Roboflow, Edge Impulse, and TensorFlow Lite for data preprocessing and model training to leverage proven, efficient solutions.
2. **Local Execution**:
Allowing users to trigger model execution on local CPUs provides flexibility and autonomy in deploying the system.
3. **Dual Hardware Variants**:
Choosing Raspberry Pi and AWS Snowcone as hardware variants provides a spectrum of deployment options to cater to diverse user needs.
4. **Integration with Platforms**:
Collaborating with Wildlife Insights, TrapTagger, Trapper, iNaturalist, Cantrap DP, and GBIF ensures a comprehensive and interconnected ecosystem.

## Implementation:

1. **Data Preprocessing and Training**: Utilization of third-party services involves integrating APIs and SDKs for seamless data processing and model training.
2. **Prediction Engine**: Deployment of trained models on selected hardware variants (Raspberry Pi or AWS Snowcone) for efficient and accurate species predictions.
3. **Model Repository**: Implementation of a secure central repository for storing and managing model checkpoint files, ensuring accessibility and security.
4. **User Interaction**: Designing a user-friendly interface for triggering model execution and facilitating interactions with camera trap labeling platforms.
5. **Security Measures**: Implementation of encryption and access controls for safeguarding model checkpoint files in the repository.

## Consequences:

1. **Increased Efficiency**: The AI-based system significantly reduces the time and effort required for species identification, enabling more efficient conservation monitoring.
2. **User Empowerment**: Offering a choice between Raspberry Pi and AWS Snowcone empowers users to make decisions based on their specific requirements and constraints.
3. **Collaborative Impact**: Integration with various platforms fosters collaboration with experts, citizen scientists, and global biodiversity initiatives, amplifying the impact of conservation efforts.
4. **Data Exchange Standardization**: Implementing data exchange standards like Cantrap DP enhances interoperability and ensures compatibility with broader conservation data ecosystems.
