## Failure handling:
-  I want to group all kinds of failures into a few category. For e.g

   - Connectivity failure 
      -  Due to server being unreachabe
      -  Due to no internet connection
      -  Due to slow internet connection
      -  Socket failure

   - Backend Failure 
      - (must contains response code and optionaly contains message)
      
   - Source Code/Unknown Failure
   - Parsing Failure

### Concerns that i want to eradicate while handling failure
    - Defining new failure
    - Throwing them from various context
    - Catching them
    - Wrapping with failure widget over and over again

### Concerns I want to deal with
    - What to do on any given failure event from aforementioned      failurs. 

    - Emitting failure state

### Flexibility I want to provide
    - I want to facilitate any UI reaction like showing floating widget (e.g. dialog, snackbar), navigation to route, replacing or adding any widget.

#### Note: 
Any kind of ambiguity should be avoided.