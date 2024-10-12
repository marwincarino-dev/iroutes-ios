# iroutes-ios

> [!NOTE]
> Project: https://github.com/users/marwincarino-dev/projects/2

## Story: User requests to see the fastest route from location A to location N
### Narrative #1
```
As a user with internet connection
I want to see my current location on a map
So I know where I am
```
### Scenarios
```
Given the user has internet connection
When the user opens the app
Then app should display maps screen
And display user's current location

Given the user has no internet connection
When the user opens the app
Then app should display routes screen
And display user's saved routes
```

### Narrative #2
```
As a user
I want to search for a location
So I can see the fastest route from my current location to that location
```
### Scenarios
```
Given the user is in map screen
When the user enters a location
Then the app should display fastest route from user's current location to that location
```

### Narrative #3
```
As a user
I want to search for multiple locations
So I can see the fastest route from location A to location N
```
### Scenarios
```
Given the user is in map screen
When the user enters multiple locations
Then the app should display fastest route from location A to location N
```

### Narrative #4
```
As a user
I want to select a saved route
So I can view it anytime
```
### Scenarios
```
Given the user has internet connection and is in routes screen
When the user selects a route
Then the app should display map screen with selected route

Given the user has internet no connection and is in routes screen
When the user selects a route
Then the app should display route details screen with selected route
```

### Narrative #5
```
As a user
I want to save a route
So I can select it anytime
```
### Scenarios
```
Given the user is in map screen
When the user saves a route
Then the app should save the route in a local storage
```

### Narrative #6
```
As a user
I want to edit a route
So I can update it
```
### Scenarios
```
Given the user is in map screen displaying the selected route
When the user taps update
Then the app should display editing mode
And allow user to save or discard changes
```

## Search Use Case
### Data
- Location

### Primary Course (Happy Path)
1. The user enters a location
2. The app shows suggested locations on search results
3. The user selects a location from the search results
4. The app shows fastest route base on selected locations

### Invalid Data - Error Course (Sad Path)
1. The user enters a location
2. The app queries for the location
3. The app is unable to suggest locations
1. The app shows empty state on search results list

### No Internet Connection - Error Course (Sad Path)
1. The user enters a location
2. The app is unable to query for the location
3. The app shows error state on search results list
