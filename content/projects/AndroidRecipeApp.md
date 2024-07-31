+++
title = 'Android Recipe App'
draft = false
summary = "This project, part of the **Platform Based Development** course, involved developing an Android app for managing cooking recipes. The app enables users to browse online recipes filtered by the main ingredient, view recipe details, mark recipes as favorites, and access favorite recipes offline. The project encompasses various Android development components and classes to deliver a functional and user-friendly application."
featured_image = "images/recipeApp.png"
+++

### Description

This project, part of the **Platform Based Development** course, involved developing an Android app for managing cooking recipes. The app enables users to browse online recipes filtered by the main ingredient, view recipe details, mark recipes as favorites, and access favorite recipes offline. The project encompasses various Android development components and classes to deliver a functional and user-friendly application.

### Main Features

1. **Browse Recipes by Ingredient:**

   - Users can search for recipes by selecting a main ingredient. The app fetches matching recipes from [TheMealDB API](https://www.themealdb.com).

2. **View Recipe Details:**

   - Detailed information about each recipe, including ingredients, measures, and preparation instructions, is available.

3. **Mark as Favorites:**

   - Users can mark recipes as favorites, making them accessible even when offline.

4. **Offline Access to Favorites:**
   - The app stores favorite recipes in a local Room database, ensuring they are available without internet connectivity.

### Components and Key Concepts

#### Splash Screen

- **SplashActivity:**
  - Displays a splash screen for 2 seconds before navigating to MainActivity.
  - Layout file: `activity_splash.xml`.

#### Main Screen

- **MainActivity:**

  - Uses `CoordinatorLayout` with `AppBarLayout` and `TabLayout` for navigation.
  - Contains a `ViewPager2` connected with `SectionsPagerAdapter`.
  - Layout file: `activity_main.xml`.

- **SectionsPagerAdapter (FragmentStateAdapter; adapter):**
  - Manages the fragments displayed in `ViewPager2`.

#### Search Functionality

- **SearchFragment:**

  - Allows users to search recipes by main ingredient.
  - Displays search results in a `RecyclerView` grid with images and titles.
  - Layout file: `fragment_search.xml`.

- **SearchViewModel:**
  - Handles data operations, interacting with `RecipeRepository` to fetch recipes.
- **Adapters:**
  - **SpinnerAdapter:** Populates the ingredient list in a `Spinner`.
  - **RecyclerViewAdapter:** Manages recipe summary items in the `RecyclerView`.

#### Favorites

- **FavoritesFragment:**

  - Displays favorite recipes from the local Room database.
  - Layout file: `fragment_favorites.xml`.

- **FavoritesViewModel:**
  - Manages favorite recipes data, interacting with `RecipeRepository`.

#### Recipe Details

- **DetailsActivity:**

  - Shows detailed recipe information, fetched either from the API or the local database.
  - Allows users to add or remove recipes from favorites.
  - Layout file: `activity_details.xml`.

- **DetailsViewModel:**
  - Manages the recipe details data.

### Data Management

- **Repository Pattern:**

  - **RecipeRepository:** Handles API calls and database interactions.

- **Room Database:**

  - **Database:** Manages database instantiation.
  - **RecipeDao:** Defines database access methods.
  - **RecipeDetails (entity):** Represents recipe details in the database.

- **Retrofit2:** Used for API communication with [TheMealDB](https://www.themealdb.com).

  - **RestAPI:** Defines API endpoints.
  - **ServiceGenerator:** Creates Rest API clients.

- **Data Transfer Objects (DTOs):**

  - **RecipeDetailsDTO, RecipesByIdDTO, RecipeSummaryDTO, RecipesByIngredientDTO:** Convert JSON data to Kotlin objects.

- **Intermediate Models:**
  - **RecipeDetailsIM, RecipeSummaryIM:** Hold data from either the server or local database.

### Implementation Details

- **Error Handling:** Errors are managed with user-friendly messages.
- **Offline Functionality:** Favorite recipes are accessible without an internet connection.
- **UI Enhancements:** Swipe-to-refresh, scrollable content, and improved interface design.

### Video Demonstration

{{<videoPortrait src="/videos/androidRecipeApp.webm" type="video/webm" preload="auto" >}}
