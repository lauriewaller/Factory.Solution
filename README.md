# Factory Application

#### An application using a many-to-many relationship to track a factory's engineers and machines 

#### By **Laurie Waller**

## Technologies Used

* C#
* ASP.NET Core MVC
* ASP.NET Razor
* Entity Framework Core
* .NET 5
* MySQL 
* MySQL Workbench
* CSS
* HTML5

## Description
This application allows the user to track stylists and clients at their salon. Users can add new stylists and clients, view all stylists and clients, view details for a stylist, and view clients who belong to a specific client. 

## Database Structure 

![image](https://user-images.githubusercontent.com/57472714/119250300-fe6a6f80-bb53-11eb-97e7-83deee75d5ef.png)

## Prerequesites
* [.Net Framework](https://dotnet.microsoft.com/download/dotnet/thank-you/sdk-2.2.106-macos-x64-installer)

## Setup/Installation Requirements

  1. Go to the main page of the repository (https://github.com/lauriewaller/Factory.Solution).
  2. In the top righthand corner of the list of files, click the Code dropdown menu.
  3. Click on the clipboard icon to copy the URL to the GitHub repo.
  4. On your computer, open Terminal and navigate to the folder where you plan to clone the repo folder.
  5. Type in `git clone` and then paste the URL you copied:
      `git clone https://github.com/lauriewaller/Factory.Solution`. Press Enter.
  6. One great application to open your files in is Visual Studio Code. To download VS Code, go to https://code.visualstudio.com/ and click on Download in the top righthand corner. From there, choose the download type necessary for your computer and follow the prompts.
  7. After you have completed the VS Code download, return to Terminal. Once you've ensured you are still in the root directory of the folder you want to open, type `code .` and press Enter. This will open the application files in VS Code for you.

  8. In the Factory directoy, create the file `appsettings.json`. Add the following code and save the file:

    {
      "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=laurie_waller;uid={INSERT_USERNAME};pwd={INSERT_PASSWORD};"
      }
    }

  9. To set up the database, run these commands in MySQL:
  
    CREATE SCHEMA `laurie_waller`;
    USE laurie_waller;
    CREATE TABLE `laurie_waller`.`stylists` (
    `StylistId` INT NOT NULL AUTO_INCREMENT,
    `Name` VARCHAR(255) NULL,
    `Schedule` VARCHAR(255) NULL,
    PRIMARY KEY (`StylistId`)
    );
    CREATE TABLE `laurie_waller`.`clients` (
    `ClientId` INT NOT NULL AUTO_INCREMENT,
    `Name` VARCHAR(255) NULL,
    `PhoneNumber` VARCHAR(255) NULL,
    `Address` VARCHAR(255) NULL,
    `StylistId` INT NULL DEFAULT 0,
    PRIMARY KEY (`ClientId`)
    );

  8. In Terminal, navigate to the Factory directory and type in `dotnet restore` and `dotnet build` to restore dependencies and compile code.

  9. In Terminal, type in `dotnet run` to run the program. 


## Known Bugs

* No known errors

## License

MIT

Copyright (c) 2021 by Laurie Waller

## Contact Information

_Laurie Waller (lauriewaller7@gmail.com)_
