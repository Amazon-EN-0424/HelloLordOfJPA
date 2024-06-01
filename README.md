# Lord of JPA

![](./elf.png)
# Objective
Create a Spring Boot project that allows you to store and retrieve information about characters and locations from the Lord of the Rings universe using Spring Data JPA and custom queries.

## Requirements

### Set up a new Spring Boot project with the necessary dependencies
- Spring Data JPA
- H2 Database

### Create the following entities
- **Character**: Represents a character from Lord of the Rings. It should have properties such as `id`, `name`, `race`, and `age`.
- **Location**: Represents a location in Middle-earth. It should have properties such as `id`, `name`, and `description`.

### Create repository interfaces for each entity using Spring Data JPA
- **CharacterRepository**: Extends `JpaRepository<Character, Long>`
- **LocationRepository**: Extends `JpaRepository<Location, Long>`

### Implement the following custom queries using the repository methods

#### CharacterRepository
- Find characters by race
- Find characters by age range
- Find characters by name containing a specific keyword
- Find characters by race and age greater than a specific value

#### LocationRepository
- Find locations by name
- Find locations by description containing a specific keyword
- Find locations by name starting with a specific prefix
- Find locations by name, ignoring case

### Write unit tests for the custom queries in the repositories using JUnit 5 and AssertJ

#### Test the CharacterRepository methods
- `findByRace_ShouldReturnCharacters_WhenRaceMatches`
- `findByAgeBetween_ShouldReturnCharacters_WhenAgeInRange`
- `findByNameContaining_ShouldReturnCharacters_WhenNameContainsKeyword`
- `findByRaceAndAgeGreaterThan_ShouldReturnCharacters_WhenRaceAndAgeMatch`

#### Test the LocationRepository methods
- `findByName_ShouldReturnLocation_WhenNameExists`
- `findByDescriptionContaining_ShouldReturnLocations_WhenDescriptionContainsKeyword`
- `findByNameStartingWith_ShouldReturnLocations_WhenNameStartsWithPrefix`
- `findByNameIgnoreCase_ShouldReturnLocations_WhenNameMatches`

### Populate the database with sample data for characters and locations from the Lord of the Rings universe using a data loader

#### Create a DataLoader class that implements the CommandLineRunner interface
- In the `run` method, create instances of Character and Location with sample data.
- Use the CharacterRepository and LocationRepository to save the sample data to the database.

## Instructions
1. Start by setting up a new Spring Boot project with the required dependencies.
2. Create the Character and Location entities based on the provided requirements.
3. Implement the CharacterRepository and LocationRepository interfaces, extending JpaRepository and adding the custom query methods.
4. Write unit tests for the custom queries in the repositories using JUnit 5 and AssertJ, following the specified test case names and scenarios. Ensure that the tests cover the different query methods and verify the expected results.
5. Create a DataLoader class that implements the CommandLineRunner interface. In the `run` method, create instances of Character and Location with sample data from the Lord of the Rings universe. Use the CharacterRepository and LocationRepository to save the sample data to the database.
6. Run the application and verify that the data loader populates the database with the sample data.
7. Run the unit tests and ensure that all the tests pass, confirming the correctness of the custom queries.
```