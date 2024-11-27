# rr-digital-project-
I developed a multi-step form application that guides users through a comprehensive identity verification process. My primary goal was to create a user-friendly, step-by-step experience that collects personal, contact, and document information while maintaining a smooth navigation flow.
I started by implementing session state management to track the user's progress through the form. 
In the initialize_session_state() function, I set up a system to store form data and track the current step.
This allowed users to move back and forth between form sections without losing previously entered information.
I designed a progress bar and step indicator using the render_progress_bar() function. 
This visual element helped users understand where they were in the form-filling process, showing them which of the four total steps they were currently completing.
The form was broken down into four distinct steps:
Personal Information Step: Here, I collected crucial personal details like given name, family name, date of birth, and tax ID.
I implemented form validation to ensure all required fields were filled before allowing progression to the next step.
Contact Information Step: In this section, I gathered address details including street address, city, state, and postal code.
I added a state dropdown with pre-populated options and included navigation buttons to move back to the previous step or proceed forward.
Document Verification Step: This step allowed users to select their document type, enter a document number, and upload a supporting document.
I supported various file types like PDF, PNG, and JPEG, and provided a preview of the uploaded document.
Review Step: The final stage presented all collected information for user review. Users could verify their details, go back to make changes, or submit the form. Upon submission,
I included a placeholder for backend data processing, currently displaying the collected information as a JSON object.
Throughout the application, I used Streamlit's session state management (st.session_state) to persistently store form data. This meant that if a user navigated back to a previous step, their previously entered information would still be there.
I implemented form submission buttons with conditional logic to enforce data validation. Users could only proceed to the next step or submit the form if all required fields were filled. Error messages were displayed to guide users in completing the form correctly.
The main function orchestrated the entire flow, rendering the appropriate step based on the current st.session_state.step value. This created a dynamic, interactive form-filling experience.
While this implementation is a frontend demonstration, in a real-world scenario, the form would typically send the collected data to a backend service for further processing, such as identity verification or database storage.
i hosted this on gradio and here is the link for gradio'huggingface-https://huggingface.co/spaces/sidhtang/kyc_
