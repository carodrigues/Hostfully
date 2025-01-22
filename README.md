# Hostfully
Hostfully Booking project 

# Environment setup

1- **Download and install Git** and configure it on your system.
   * Download Git from https://git-scm.com/.

2- **Access GitHub**.
   * Github site: https://github.com/

3- **Clone the repository** to your local computer using the following command:
  ```bash
   git clone https://github.com/carodrigues/Hostfully.git
  ```
4- **Download and Install the latest version of Postman** (Windows 64-bit).  
   * Dowload Postman from https://www.postman.com/downloads/.

5- **Start Postman** and log in with a valid account.

6- **Import the collection**: Postman\Hostfully.postman_collection.json.
   * To import, go to File → Import and select the file.


# How to Execute the Test Cases

# Preconditions
* Ensure that the database is empty!
* Execute the API calls, one by one, by the refered order 

# Test Execution Plan
The tests to be executed are numbered from **1 to 16**.

## First Round: obain bookings with database empty
The **first round of tests** consists of two API calls aimed at validating the response when no property exists in the database.


![image](https://github.com/user-attachments/assets/343740ed-02aa-4c6d-9800-7382393a28a6)


After completing the first round of tests, you can proceed to validate **Property Creation**.

## Second Round: POST new properties 
The **second round** is designed to test the creation of new properties, including both success and failure cases.

![image](https://github.com/user-attachments/assets/4a8847ac-6eb5-4fa5-ac1f-8d5a2d6e57a1)


## Firth Round: Booking Validation
The **firth round** focuses on **Booking Validation**, ensuring that:
* ***API call 17*** Before creating a new booking, verification is conducted to confirm that the new booking does not overlap with existing ones for a specific guest.
* ***API call 18 and 19*** validate that post follow verifies overlap cases

![image](https://github.com/user-attachments/assets/3c1369c3-6f8b-4a43-aacc-2cb75504250e)



