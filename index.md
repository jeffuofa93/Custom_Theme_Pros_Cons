# Pros and Cons Drupal Custom Theme vs Asset Injector

## Pros Custom Theme

- Drupal best practice for adding multiple javascript/css files and modules
- Allows control and customization for how files load, on which pages and where they loaded in the page
    - We will understand how the modules are interacting and will be able to debug issues to a with support from
      drupal 9 online resources
      
- Multi developer workflow improved
    - Allows two developers to work on the same file without causing issues inside Drupal
    - Any changes to files on the site would be well documented via git
    - 
- File organization improved
    - Custom theming allows for the storage of js and cs files inside custom files and folders
    - Files are seperated from modules which is valuable distinction not present in asset injector
  
- Long term maintainability Site Organization
  - With current MVP of page builder we have 14 js/css files in the Asset Injector, and an undocumented amount of
    html src imports inside pages. We have already felt this pressure with the small number of files in Page Builder and it will grow over time.
  - With a custom theme it is organized and easy to maintain and extremely large amount of internal and external 
    javascript/css files and modules

- Design enforcement of best practices
  - With a custom theme there are no alternatives to setting up local dev environments using lando and pushing and 
    pulling changes to the code base which is the ideal configuration for long term stability of the site
  - This functionality is possible with Asset Injector, but it's much easier initially to modify files directly in 
    drupal which creates issues regarding maintainability, site organization, multi developer workflow, and change 
    documentation


## Cons Custom Theme

- We don't know what we don't know
    - We have just started learning about Drupal custom themes and as a team this will be new for everyone
    - Digital Learning has built successful websites with Asset Injector 
      
- Site breaking failures 
    - If we experience bugs or errors with a custom theme it can break the design for the entire site
    - This is unlikely to happen but objectively it's more likely for our team to make mistakes vs 
      the active maintainers of a popular drupal extension
      
- Complexity of applying files or modules to specific pages 
    - Unlike Asset Injector where we can simply select the page to apply a file to, with a custom theme we have to use 
    php code inside the theme itself.
      
- Long term maintainability Custom Theme Management 
    - Due to Digital Learning employing student developers their will be different students working on 
      projects and entering and leaving the team
    - The overhead of training an employee to manage the custom theme is much higher than teaching how to use 
      Asset Injector. With poor planning or an emergency it's possible to end up in a position where no one on the 
      team knows how to use the backend of the custom theme. 
      
      
