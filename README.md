# ObjectIDReservations

Do not modify reservations.txt by hand; use the PowerShell module instead!

## Installation
- Make sure you have a GitHub account that is associated with the Mprise Indigo organization;
- Make sure you have a working Git installation on your machine;
- Clone https://github.com/mprise-indigo/ObjectIDReservations to your machine;
- Install the required PowerShell module by running `Install-Module UncommonSense.Nav.ObjectIDReservations -Scope CurrentUser`.
- Add default values to your PowerShell profile for the following parameters. An easy way to do this is to load `Agriware 2015\InternalDocs\TeamProfile.ps1` from the script whose path is returned by `$Profile.CurrentUserAllHosts`.
  - ErrorAction should be set to 'Stop'
  - DataFilePath should be set to the path of your local copy of reservations.txt from the ObjectIDReservations repo;
  - BeforeLoad should return a scriptblock that `git pull`s server changes into your local ObjectIDReservations repo;
  - AfterSave should return a scriptblock that `git commit`s, then `git push`es local changes into the ObjectIDReservations repo.
