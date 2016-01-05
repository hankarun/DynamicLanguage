# DynamicLanguage

This is an example of changing the languange of an Android App in runtime. Source is extracted mostly from Signal-Android Messenger.

Product structure is factoring Baseclassa and create a Precreate method to set the local at runtime. Each of the activity in this case there is one checks the local configured in sharedpreferences, then it sets the local before view created.

Preferences class also extracted as a static class from same source. All of the preference methods encapsulated inside a static class.

Dynamic language class is responsable of getting Activity as parameter and set its local. It has onCreate and on Resume methods. OnCreate methods can be called when the activity first created. OnResume is to set local again if it changed from previus savedstate. VERSIONS under 11 uses new intent to update activity but for 11 above activies reacreate method is using.

Ali Iskender Turan
