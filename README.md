# Memorable's Systems Design Technical Test: Creative Scoring Platform

### Overview:

The objective of this test is to design a robust web platform capable of managing, tagging and scoring images using a set of predefined endpoints. The platform should be user-friendly, scalable, and adaptable to future requirements. 

You are not required to code for this interview. You should assume that you are building a detailed set of design documents that will be used as ground truth reference by your team to implement this product. The documents should include, at a minimum, a complete readme with the stack used, set of functionalities enabled and overall design, as well as a system and database diagram of the application. You can add more documents and even code snippets if you'd like. You will be asked to present your design in a follow-up meeting.

### Core Functionalities:

1. **Image Upload**: Users should be able to upload images via a simple frontend interface.
2. **Image Processing**:
    - Score images based on visual-only metrics. You can assume that an endpoint already exists that receives an image, runs a machine learaning model, and returns a set of N scores. The endpoint always returns N scores, for any image.
    - Automatically tag the images based on the model's output. You can assume that an endpoint already exists that receives an image, runs a model and returns T tags for the image. The number of tags can vary per image.
3. **Image Management**:
    - View a list of uploaded images.
    - Organize images into folders for better management.
    - View an image’s score and tags.
4. **Tag Editing**: Users should have the capability to manually correct or edit the tags assigned to images.
5. **User management:** Different users should be able to sign in, log in, log out, and view their own images. 

### Constraints:

- **Organizational Structure**: Users are grouped into organizations. Any user within an organization should have access to images uploaded by their peers.
    - Model outputs and scoring metrics may vary depending on the organization.
- **Model Versioning**: It's essential to keep track of model versions when scoring images. Keep that in mind when designing how to store the outputs of the tagging and scoring endpoints. You can assume that these endpoints return the model_version at each call.
- **Reprocessing**: When a new model version is released, previously uploaded images should be reprocessed to reflect updated scores.
- **Monitoring**: Implement a system to monitor the processing status of assets, ensuring system health and timely error detection.
- **Concurrency**: The system should support 'N' users uploading and processing assets simultaneously.
- **Efficiency**: Given that metrics computation can be slow and resource-intensive, the system should be optimized for users who might open the same page multiple times.

### Deliverables:

The point of this exercise is to generate design documents that can help a team of developers develop the entire application - the deliverables are documents and diagrams explaining the implementation. To submit your solution, please **fork this repository, commit your files and add @cfosco, @ppfreitas as contributors.**.

At a minimum, your repo should contain:
- **Project Readme:** explanation of the project. Stack to be used, set of functionalities and overall design description.
    - **Endpoint List**: A comprehensive list of all API endpoints with their respective functionalities.
    - **Testing Plan**: A strategy to ensure the system's functionality, performance, and security.
    - **Task Definition to execute the project**: A breakdown of tasks and their respective workflows.
    - **Security considerations**: Details on architectural and functional choices to ensure that the app and infrastructure powering it is secure.
- **System Diagram**: A visual representation of the entire architecture.
- **Database Diagram**: A visual representation of the database schema and relationships.

**Optional**

- **Frontend Structure**: A high-level overview of the frontend components and their interactions. No code required, just a diagram or document detailing the components.
- **Logging System**: A mechanism to capture, store, and analyze system logs.
- **User Authentication**: A secure system to manage user sign-ups, logins, and permissions.
- **Infrastructure Diagram**: A detailed diagram showcasing all infrastructure components.