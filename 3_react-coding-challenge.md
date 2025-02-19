**Challenge: Simple React Component**

You are now tasked with building a react component to display patients in a table and provide a means of marking individual patients as reviewed. Only the component's code needs to be produced, the component does not need to be integrated into a development site.

**Requirements:**

1.  **Create a simple react component:** Create a react componet that accepts an array of Patients as a property and displays their information in a table. 

2.  **Reviewed state toggle:** Each patient table row will have a button toggle reviewed state. Each patient will be "Unreviewed" at first, but when the button is clicked the button text will change to "Reviewed". Clicking the button again will revert to "Unreviewed". 
 
3.  **Patient Interface:** We will use the same Patient interface from the TypeScript challenge.

    *   `id` (number, required): The unique ID of the patient.
    *   `name` (string, required): The name of the patient.
    *   `age` (number, required): The age of the patient.
    *   `diagnosis` (string, required): The patient's diagnosis.
    *   `admissionDate` (string, optional): The date of admission (you can use a string format like "YYYY-MM-DD").

4.  **Bonus:** Demonstrate the component (using mock Patient data) in a development site or storybook page.