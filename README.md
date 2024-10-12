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

### Narrative #7
```
As a user
I want to delete a route
So it is removed from my routes screen
```
### Scenarios
```
Given the user is in map screen displaying the selected route
When the user taps delete
Then the app should display confirmation
And allow user to cancel or confirm action

Given the user is in routes screen
When the user swipes on a route
Then the app should display confirmation
And allow user to cancel or confirm action
```

## Search Use Case
### Data
- Location

### Primary Course (Happy Path)
1. The user enters a location
2. The app queries for the location
3. The app shows suggested locations on search results
4. The user selects a location from the search results
5. The app shows fastest route base on selected locations

### No Internet Connection - Error Course (Sad Path)
1. The app is unable to query for the location
2. The app shows error state on search results list

### Invalid Data - Error Course (Sad Path)
1. The app is unable to suggest locations based on queried location
2. The app shows empty state on search results list

## Save Route Use Case
### Data
- Route

### Primary Course (Happy Path)
1. The user is viewing a route
2. The user taps save
3. The user add route name
4. The user taps confirm
6. The app saves the route on local storage

### Unable to Save - Error Course (Sad Path)
1. The app is unable to save the route in local storage
2. The app shows an error message

## Select Route Use Case
### Data
- Route

### Primary Course (Happy Path)
1. The user selects route from routes screen
2. The app shows route on map screen

### No Internet Connection - Error Course (Sad Path)
1. The user selects route from routes screen
2. The app shows route on route details screen

## Edit Route Use Case
### Data
- Route

### Primary Course (Happy Path)
1. The user is viewing a route
2. The user taps edit
3. The app shows editing mode
5. The user taps save
6. The app updates the route on local storage

### Unable to Update - Error Course (Sad Path)
1. The app is unable to update the route in local storage
2. The app shows an error message

## Delete Route Use Case
### Data
- Route

### Primary Course (Happy Path)
1. The user is viewing a route map screen
2. The user taps delete
3. The app shows confirmation dialog
5. The user taps confirm
6. The app deletes the route from local storage

### Primary Course (Happy Path)
1. The user swipes a route in routes screen
2. The user taps delete
3. The app shows confirmation dialog
5. The user taps confirm
6. The app deletes the route from local storage

### Unable to Delete - Error Course (Sad Path)
1. The app is unable to delete the route in local storage
2. The app shows an error message
