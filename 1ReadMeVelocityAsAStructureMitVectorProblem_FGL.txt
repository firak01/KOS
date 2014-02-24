    Velocity is not a vector, It is a structure with a few vectors in it
    http://erendrake.github.io/KOS/structure/vessel/

    This is the new documentation site that we started this weekend and will keep working on

    Quote Originally Posted by J.Random View Post
    Terminal window input conflicts with HullCameraVDS controls (-/=/BS).
    What would you like us to do about this? 

Reply With Quote Reply With Quote
19th February 2014, 03:54 #223
J.Random
J.Random is offline
Spacecraft Engineer J.Random's Avatar

Join Date
    May 2013
Location
    Moscow, Russia
Posts
    201	

    Quote Originally Posted by erendrake View Post
    We have been talking about lately how to deal with the inconsistency in reference frame that the KSP API presents to us and how we want to abstract away the crazy from kOS scripters. Expect more of this in weeks to come.

    Velocity is not a vector, It is a structure with a few vectors in it
    http://erendrake.github.io/KOS/structure/vessel/
    Ah, that's what got me confused. If you type `print velocity.`, you will get only the first vector as output (in form of V(double,double,double), it seems), and you won't be able to do anything with it. velocity:{orbit,surface}:{x,y,z,mag} works, thanks.

    What would you like us to do about this?
    Well, from some early version I remember a bug when typing in terminal would stage vessel, kill throttle, etc. You can't block hooks installed by other mods from execution? If not - sorry, didn't know that. 

############################################################################################################

 Quote Originally Posted by Steven Mading View Post
The problem with the word "velocity" isn't frame of reference (which direction the XYZ axes point and where the origin is).
Im sorry i might have been unclear, right now.
PRINT SHIP:VELOCITY.

returns the string representation of the orbitalvelocity vector, what i was considering removing was the string that you cannot use as a vector because it is a string, I was thinking instead for structures to return.

PRINT SHIP:VELOCITY.
Type: VesselVelocity. Members: ORBIT, SURFACE.

so everyone doesnt have to run to the web every time they cannot remember the manyfold members of VesselTarget.