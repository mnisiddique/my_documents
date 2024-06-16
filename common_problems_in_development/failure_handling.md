# Problem Statement:
Deriving a scalable way to handle failures in flutter. Or finding a pattern for handling failures in flutter


 ### What do i want?
 ### Ans: 
  I want different handlers to handle different failures. 
  I am assuming that, each different handers are bloc listener.
  I would inject them somehow to the list of Multibloc listener.
  
  The problem with that approach is, bloc listeners are very specific to
  the bloc. But the failure handling logic is not connected to any bloc.
  Perhaps they are connected to feature or they could be generic to whole app.
  
  Failures that require to be handled from ui requires context.
  UI change caused by failure handling can be of following category
  1. Change of current UI.
     Note: Generally done using BlocBuilder

  2. Showing anything on top of current UI
     Note: Generally alert, dialog, popups, snackbars etc.

  3. Navigation
  
