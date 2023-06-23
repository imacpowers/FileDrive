# File Management Application

This application allows users to manage their files by providing a search bar and sort functionality. Users can easily find and organize their files based on their preferences.

## Search Bar Functionality

The search bar allows users to search for specific files within their collection. Here's how the search functionality works:

1. Enter the name or a part of the name of the file you want to search for in the search bar.
2. As you type, the application dynamically filters the file list to display only the files that match the search query.
3. The search is case-insensitive, meaning it will match files regardless of their capitalization.
4. The search query matches against the file names, and any files with names containing the search query will be displayed.

For example, if you enter "document" in the search bar, the application will show all files with "document" in their names, such as "my_document.docx" and "important_documents.pdf".

## Sort Functionality

The sort functionality allows users to organize their files based on different criteria. Currently, the application supports sorting files by the following options:

- **Name**: Sorts the files alphabetically by their names.
- **Size**: Sorts the files based on their sizes, from smallest to largest.
- **Type**: Sorts the files alphabetically by their types (e.g., video, audio, document, image).

Here's how to use the sort functionality:

1. Locate the "SortBy" dropdown menu in the control tools section.
2. Click on the dropdown menu to reveal the available sort options.
3. Select the desired sort option from the dropdown menu.
4. Once a sort option is selected, the files will be rearranged based on the chosen criteria.
5. The sorting is applied instantly, and the file list will be updated accordingly.

For instance, if you choose to sort by "Size," the application will display the files in ascending order based on their sizes, starting from the smallest file.

Please note that the sort functionality allows only one sort criteria at a time. To change the sorting criteria, repeat the steps above and select a different option from the dropdown menu.

#  **Why the Search bar and Sort Functionalities were added to the Multimedia Web App**

The Multimedia Web App is designed to provide users with a convenient and efficient way to manage their multimedia files. To enhance the user experience and improve file organization, the following features have been incorporated into the application:

## Search Bar Functionality

The search bar functionality is an essential addition to the Multimedia Web App for the following reasons:

1. **Efficient File Search**: As users accumulate a large number of multimedia files, manually browsing through the entire collection becomes time-consuming and tedious. The search bar allows users to quickly locate specific files by entering a search query. This significantly improves the efficiency of file retrieval.

2. **Intuitive User Experience**: The search bar provides a familiar and intuitive way for users to interact with the application. Users are accustomed to using search bars in various applications, such as search engines and file explorers. By incorporating a search bar, the Multimedia Web App aligns with user expectations and makes the file management process more intuitive.

3. **Flexibility in File Retrieval**: The search bar supports partial matching, enabling users to search for files based on specific keywords or even fragments of file names. This flexibility ensures that users can retrieve files even if they don't remember the exact file names or want to search for files with similar names.

## Sort Functionality

The sort functionality is another valuable addition to the Multimedia Web App due to the following reasons:

1. **Improved File Organization**: As users accumulate a diverse collection of multimedia files, organizing them becomes crucial. The sort functionality allows users to sort their files based on different criteria such as name, size, and type. This enables users to arrange files in a way that makes sense to them and facilitates easy access.

2. **Personalization and Customization**: Each user may have different preferences for how they want their files to be organized. By providing multiple sort options, the Multimedia Web App allows users to personalize their file organization based on their specific needs. This customization enhances the user experience and accommodates individual preferences.

3. **Enhanced User Productivity**: Sorting files based on specific criteria can help users identify patterns, find duplicates, or quickly locate files of a particular type or size. This promotes productivity by reducing the time and effort required to manually search through the file list. Users can easily identify and access files based on their sorting preferences.

By incorporating the search bar functionality and the sort functionality, the Multimedia Web App aims to streamline the file management process, improve user productivity, and provide a user-friendly experience for organizing multimedia files.

## How does the code work?
**Importing Dependencies:**

The code begins by importing the necessary dependencies for the React application, including React itself and various components and libraries used in the app.

**State Initialization:**

The useState hook is used to initialize several state variables that will hold the application's data and control its behavior. These variables include myFiles, selectedFile, filePath, sortBy, showChartModal, and searchQuery.
The myFiles state variable stores the array of files retrieved from the data file.
The selectedFile state variable stores the currently selected file.
The filePath state variable stores the current file path for displaying in the UI.
The sortBy state variable determines the sorting criteria for the file list.
The showChartModal state variable controls the visibility of the chart modal.
The searchQuery state variable holds the user's search query for filtering files.

**Fetching Initial Data:**

The useEffect hook is used to fetch the initial data from the data file and set it to the myFiles state variable.
The effect runs only once when the component mounts, ensuring that the data is fetched and set only on the initial render.

**Sorting Files:**

The sortFiles function is defined to sort the files based on the sortBy state variable.
Within the sortFiles function, the files array is sorted using a compare function that compares the files based on the selected sorting criteria (name, type, or size).
The sorted files are returned by the sortFiles function.

**Filtering Files:**

The filteredFiles variable filters the myFiles array based on two conditions:
The file path should match the current filePath state variable.
The file name should include the searchQuery state variable (case-insensitive).
The filtered files are stored in the filteredFiles variable.

**Sorting and Filtering Files:**

The sortedAndFilteredFiles variable stores the result of applying the sorting function (sortFiles) on the filtered files.
This ensures that the files are sorted according to the selected criteria and displayed in the UI.

**Handling User Interactions:**

The code includes several event handlers to handle user interactions and update the state variables accordingly.
The handleSortByChange function updates the sortBy state variable based on the selected value from the sort dropdown.
The button click event handlers handle actions such as renaming a file, displaying the chart modal, deleting a file, and downloading a file.

**Rendering Components:**

The code uses JSX syntax to render the various components of the Multimedia Web App.
The UI components include the header, control tools (search bar, sort dropdown, buttons), file list, and the file viewer.
The file list is rendered dynamically based on the sortedAndFilteredFiles array, and each file is displayed as a clickable element.
When a file is selected, its details and the appropriate viewer component (video player, audio player, document viewer, or image viewer) are displayed.







