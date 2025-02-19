**Challenge: Asynchronous Patient Data Fetching and Processing**

You are now tasked with building a simplified patient management system.  You will fetch patient data from a mock API, process it, and display it.

**Requirements:**

1.  **Data Fetching:** Create a function `fetchPatients()` that simulates fetching patient data from an API.  This function should return a `Promise<Patient[]>`.  The `Patient` interface is defined below.  Use `setTimeout` to simulate an API call.

2.  **Patient Interface:** Define a TypeScript interface `Patient` with the following properties:

    *   `id` (number, required): The unique ID of the patient.
    *   `name` (string, required): The name of the patient.
    *   `age` (number, required): The age of the patient.
    *   `diagnosis` (string, required): The patient's diagnosis.
    *   `admissionDate` (string, optional): The date of admission (you can use a string format like "YYYY-MM-DD").

3.  **Data Processing:** Create a function `processPatients(patients: Patient[])` that takes an array of `Patient` objects. This function should:

    *   Calculate the average age of all patients.
    *   Group the patients by diagnosis.  The return type should be a `Map<string, Patient[]>`, where the key is the diagnosis and the value is an array of patients with that diagnosis.

4.  **Display Patients:** Create a function `displayPatients(patientsByDiagnosis: Map<string, Patient[]>)` that takes the processed patient data (the `Map`) as input.  This function should:

    *   Log the average age to the console.
    *   Iterate through the `Map` and for each diagnosis, log the diagnosis and then list the patients with that diagnosis (name and age).  If a patient has an `admissionDate`, log it as well.

**Bonus Challenge:**

*   Implement error handling in `fetchPatients()`. Simulate an API error and handle it gracefully.
*   Add a filtering function `filterPatients(patients: Patient[], diagnosis: string)` that returns only the patients with the specified diagnosis.

**Starter Code (Optional):**

```typescript
interface Patient {
  id: number;
  name: string;
  age: number;
  diagnosis: string;
  admissionDate?: string;
}

async function fetchPatients(): Promise<Patient[]> {
  return new Promise<Patient[]>((resolve, reject) => {
    setTimeout(() => {
      resolve(mockPatients); // Replace with your actual data fetching logic
      //reject("Failed to fetch data"); // For error simulation
    }, 500); // Simulate API delay
  });
}

function processPatients(patients: Patient[]): Map<string, Patient[]> {
  // ... (implement data processing here)
}

function displayPatients(patientsByDiagnosis: Map<string, Patient[]>): void {
  // ... (implement display logic here)
}

// Main part of your code:
async function main() {
  try {
    const patients = await fetchPatients();
    const processedPatients = processPatients(patients);
    displayPatients(processedPatients);
  } catch (error) {
    console.error("Error fetching patients:", error);
  }
}

const mockPatients: Patient[] = [
  { id: 1, name: "Alice Johnson", age: 35, diagnosis: "Flu", admissionDate: "2024-03-08" },
  { id: 2, name: "Bob Williams", age: 60, diagnosis: "Heart Condition" },
  { id: 3, name: "Charlie Davis", age: 42, diagnosis: "Flu" },
  { id: 4, name: "David Garcia", age: 70, diagnosis: "Heart Condition", admissionDate: "2024-03-05" },
];

main();

```

This updated challenge uses the `Patient` interface and focuses on data relevant to patient management. The data processing and display logic should be adapted accordingly (calculating average age, grouping by diagnosis, etc.).  The structure of the asynchronous operations and the use of Maps remains the same, providing a good opportunity to practice these concepts in a different context.
