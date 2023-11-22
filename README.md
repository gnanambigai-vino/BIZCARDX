**What is OCR?**
OCR stands for Optical Character Recognition. It is a technology that extracts text from images, scanned documents, or any visual representation of text. The main purpose of OCR is to convert images of text into machine-readable text data.
In my project I am using easyOCR to extract text from “BUSINESS CARD”.
**Some key points about OCR:**
1.	**Text Extraction:** OCR is used to recognize and extract text from images, scanned documents, or other visual representations.
2.	**Machine-Readable Data**: The output of OCR is typically machine-readable text that can be used for various purposes, such as searching, indexing, or further analysis.
3.	**Applications**: OCR has a wide range of applications, including:
4.	**Document Digitization**: Converting physical documents into digital format.
5.	**Text Search**: Enabling search functionality for scanned documents or images.
6.	**Data Entry**: Automating data entry by extracting text from images.
7.	**Accessibility**: Making text content accessible to visually impaired individuals.
8.	**OCR in Python:**
        •	Python provides several OCR libraries and tools that make it easy to incorporate OCR functionality into applications.
        •	When it comes to OCR, EasyOCR is by far the most straightforward way to apply Optical Character Recognition:
        •	The EasyOCR package can be installed with a single pip command.
        •	The dependencies on the EasyOCR package are minimal, making it easy to configure your OCR development environment.
        •	Once EasyOCR is installed, only one import statement is required to import the package into your project.
        •	From there, all you need is two lines of code to perform OCR — one to initialize the Reader class and then another to OCR the image via the readtext function.
 
**Project overview**
This Streamlit web app facilitates the extraction of pertinent details from uploaded business card images using easyOCR. Users can subsequently view, edit, or remove the extracted information. Additionally, the app enables users to save this information, along with the respective business card image, in a database capable of storing multiple entries.

**Libraries/Modules used for the project**
   - Pandas - (To Create a DataFrame with the scraped data)
   - Sqlite3 - (To store and retrieve the data)
   - Streamlit - (To Create Graphical user Interface)
   - EasyOCR - (To extract text from images)
     
**Workflow**
   To get started with BizCardX Data Extraction, follow the steps below:
- Install the required libraries using the pip install command. Streamlit, sqlite3, pandas, easyocr.
- pip install [Name of the library]
- Execute the “bizcardx.py” using the streamlit run command.
 - Streamlit run bizcardx.py
- A webpage is displayed in browser, I have created the app with three menu options namely **HOME, UPLOAD & EXTRACT, MODIFY** where user has the option to upload the respective Business Card whose information has to be **extracted, stored, modified or deleted** if needed.
- Once user uploads a business card, the text present in the card is extracted by **easyocr** library.
- The extracted text is sent to get_data() function(user defined- I have coded this function) for respective text classification as company name, card holder name, designation, mobile number, email address, website URL, area, city, state, and pin code using loops and some regular expression.
- The classified data is displayed on screen which can be further edited by user based on requirement.
- On Clicking **Upload to Database Button** the data gets stored in the SQLITE3 Database. 
- Further with the help of **MODIFY** menu the uploaded data in SQL Database can be accessed for **Read, Update and Delete** Operations.
    
