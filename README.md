# ObjectIDReservations

Do not modify reservations.txt by hand; use the PowerShell module instead!

## Installation
- Make sure you have a GitHub account that is associated with the Mprise Indigo organization;
- Clone https://github.com/mprise-indigo/ObjectIDReservations to your machine;
- Clone https://github.com/jhoek/UncommonSense.Nav.ObjectIDReservations to a folder in your PowerShell module path;
- Add default values to your PowerShell profile for the following parameters:
  - ErrorAction should be set to 'Stop'
  - DataFilePath should be set to the path of your local copy of reservations.txt from the ObjectIDReservations repo;
  - BeforeLoad should return a scriptblock that `git pull`s server changes into your local ObjectIDReservations repo;
  - AfterSave should return a scriptblock that `git commit`s, then `git push`es local changes into the ObjectIDReservations repo.
