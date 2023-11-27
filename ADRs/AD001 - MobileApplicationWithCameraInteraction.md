# Title: Mobile Application for Camera Interaction

## Status:
Proposed

## Context
We are developing a mobile application that allows customers to interact with a camera system. The application needs to provide various functionalities, including user registration, login, camera control (on/off), edge model training, model uploading, communication with the camera over different methods (3G, LoRaWAN, Satellite), remote camera settings adjustment, receiving alerts, analytics sharing, species occurrences uploading to GBIF, frame publishing to iNaturalist, manufacturer feedback, and repair requests.

## Decision
We have decided to architect the mobile application using a modular and scalable approach, incorporating the following key components:

1. **User Authentication and Authorization**:
    - Utilize OAuth 2.0 for user authentication and authorization.
    - Implement role-based access control to manage user permissions.

2. **Camera Interaction Module**:
    - Implement a modular camera interaction module for functionalities like turning the camera on/off, training edge models, and uploading models.
    - Use platform-specific APIs (Android/iOS) for camera control.

3. **Communication Module**:
    - Develop a communication module that supports 3G, LoRaWAN, and Satellite communication methods.
    - Use asynchronous messaging to handle real-time communication between the mobile app and the camera system.

4. **Remote Camera Settings and Alerts**:
    - Utilize a WebSocket-based communication channel for real-time camera setting adjustments and alerts.

5. **Analytics and Integration**:
    - Implement a data analytics module to process and share analytics data.
    - Integrate with third-party platforms for analytics sharing.
  
6. **Species Occurrences and Data Upload**:
    - Integrate with the Global Biodiversity Information Facility (GBIF) API for species occurrences upload.
    - Implement a secure data upload mechanism for other platforms, such as iNaturalist.
  
7. **Manufacturer Feedback and Repair Requests**:  
    - Integrate a feedback module for users to provide feedback to manufacturers.
    - Implement a repair request feature with a ticketing system.
  
## Rationale

1. **Modular Design**: A modular design ensures flexibility and scalability, allowing easy addition of new features and updates.
2. **Standardized Authentication**: OAuth 2.0 provides a secure and standardized approach to user authentication and authorization.
3. **Platform-specific APIs**: Using platform-specific APIs ensures optimal performance and native user experiences on Android and iOS devices.
4. **Real-time Communication**: WebSocket-based communication ensures real-time updates for camera settings and alerts.
5. **Integration with External Platforms**: Integrating with GBIF and iNaturalist allows users to contribute to biodiversity databases seamlessly.

## Consequences
1. **Increased Development Time**: The modular approach may initially require more development time, but it will result in a more maintainable and extensible system.
2. **External Dependencies**: Integration with third-party platforms may introduce dependencies that need to be monitored for changes.

## References
- [OAuth 2.0 Authorization Framework](https://oauth.net/2/)
- [GBIF API Documentation](https://www.gbif.org/developer/summary)
- [iNaturalist API Documentation](https://www.inaturalist.org/pages/api+reference)
