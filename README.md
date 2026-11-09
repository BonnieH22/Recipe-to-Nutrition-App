# Recipe-to-Nutrition-App
# Recipe Nutrition Analyzer

## Project Overview

This project is a JavaFX application that allows users to search for a meal and view its recipe, cooking instructions, and nutritional information for up to 10 ingredients. The application integrates two APIs to retrieve recipe information and ingredient-level nutrition data, which is then displayed using dynamically generated bar charts.

The goal of this project was to combine API integration, data processing, and data visualization into an interactive application.

## Technologies Used

- **Java** – Application development and data processing
- **JavaFX** – Graphical user interface and bar chart visualizations
- **TheMealDB API** – Retrieves recipes, ingredients, cooking instructions, and meal images
- **Open Food Facts API** – Retrieves nutritional information for ingredients
- **Gson** – Parses JSON responses from the APIs
- **Maven** – Project compilation and dependency management

## Application Features

- Search for meals using a text input field.
- Display recipe images and cooking instructions.
- Retrieve nutritional information for up to 10 ingredients.
- Generate individual bar charts showing the available nutritional values for each ingredient.
- Use background threads to retrieve API data without freezing the user interface.
- Display results in a scrollable interface.

## How It Works

1. The user enters a meal into the search bar.
2. The application sends a request to TheMealDB API to retrieve the recipe and its ingredients.
3. Each ingredient is used to request nutritional information from Open Food Facts.
4. The JSON responses are parsed, and the available numerical nutrition values are extracted.
5. The nutritional information is displayed in JavaFX bar charts for each ingredient.

## Application Preview

![Recipe Nutrition Analyzer](images/recipe-nutrition-preview.png)

## Running the Application

The application uses Maven to compile and run the JavaFX project.

```bash
mvn clean
mvn compile
mvn exec:exec -Dexec.mainClass=cs1302uga.api/cs1302.api.ApiDriver
```

Run these commands from the project directory containing `pom.xml`. A compatible Java JDK and Maven installation are required.

## Key Skills Demonstrated

- REST API integration
- JSON data parsing
- Data extraction and visualization
- JavaFX graphical interface development
- Multithreading and asynchronous data retrieval
- Error handling and user interaction

This project demonstrates how information from multiple external data sources can be retrieved, processed, and presented through an interactive desktop application.
