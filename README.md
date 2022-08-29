# MVVM To-Do List App with Flow and Architecture Components

# MVVM Archtectre
MVVM architecture is a Model-View-ViewModel architecture that removes the tight coupling between each component. Most importantly, in this architecture, the children don't have the direct reference to the parent, they only have the reference by observables.
## TodoApp
### The App covers the following components 
![mvvm](https://user-images.githubusercontent.com/65366942/187280218-f7b9ba07-0845-4c86-af6d-15ad8d3d8f02.png)

- ### Model
It represents the data and the business logic of the Android Application. It consists of the business logic - local and remote data source, model classes, repository.
- Room
- DataStore
- Coroutines
- Flow
- Search Functionality
- ### View
It consists of the UI Code(Activity, Fragment), XML. It sends the user action to the ViewModel but does not get the response back directly. To get the response, it has to subscribe to the observables which ViewModel exposes to it.

- ### View Model
It is a bridge between the View and Model(business logic). It does not have any clue which View has to use it as it does not have a direct reference to the View. So basically, the ViewModel should not be aware of the view who is interacting with. It interacts with the Model and exposes the observable that can be observed by the View.

## Set up a new project with Kotlin and other dependencies required
- Here, we are going to set up the Android Project.

### Create a Project

- Start a new Android Studio Project
- Select Empty Activity and Next
- Name: desired name
- Package name: com.___.___
- Language: Kotlin
- Finish
  Your starting project is ready now
#### The app has following packages:
1. **data**: It contains all the data accessing and manipulating components.
2. **di**: Dependency providing classes using Dagger2.
3. **ui**: View classes along with their corresponding ViewModel.
4. **utils**: Utility classes.

#### Classes have been designed in such a way that it could be inherited and maximize the code reuse.


## Project Structure
<img width="508" alt="project-structure-mvvm-blog" src="https://user-images.githubusercontent.com/65366942/187281776-35917e89-7507-4497-9a32-78a58794ceee.png">
### Library reference resources:
1. RxJava2: https://github.com/amitshekhariitbhu/RxJava2-Android-Samples
2. Dagger2: https://github.com/MindorksOpenSource/android-dagger2-example
3. FastAndroidNetworking: https://github.com/amitshekhariitbhu/Fast-Android-Networking
4. PlaceHolderView: https://github.com/janishar/PlaceHolderView
5. AndroidDebugDatabase: https://github.com/amitshekhariitbhu/Android-Debug-Database
6. Calligraphy: https://github.com/chrisjenx/Calligraphy
7. Room: https://developer.android.com/topic/libraries/architecture/room.html

### Thanks 
#### Silas Silikhe