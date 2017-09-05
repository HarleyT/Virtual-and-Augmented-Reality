* scale for 360 videos is fixed (height and distance between eyes)
    * real time VR doesn’t have these constraints
    * can be beneficial to take video from a seated height, as there is less variation in user heights at that level
* world moving with user (as opposed to user moving and getting a different perspective) can be a nauseating experience
* can take 360 stereoscopic images with a regular camera, or render a 3D scene and use a virtual camera
* IPD - inter-pupillary distance
* stereoscopic - each eye is seeing something different (as opposed to monoscopic)
* things that are naturally 3D that we currently show in 2D (e.g. building designs) are prime candidates for VR

* consider orientation when starting an experience
    * example of room before longbow game to gauge user’s orientation and adjust actual start of experience accordingly
* design surfaces to discourage people leaving a certain area, even small boundaries make people reluctant to leave the area (spatial geometries are generally respected)
* user needs some sort of indication of where they can and can’t go in the case of teleporting (red and green squares on floor area in demo)
* 90fps === 12ms per frame
    * any less on a high end device can make an experience nauseating
* even though you can’t consciously perceive 90fps, anything less will feel less real/immersive
* unity is best for VR currently due to forward rendering (or unreal with the beta forward rendering enables)
    * unity also has a larger community and asset store due to being free for longer

* why is a thing a thing -> lightswitch
* when using similar concepts to computers and 2D, ask yourself if you have the same constraints or if you can make it differently
    * e.g. a menu - what does a menu do, can we do it differently in VR? Can we throw objects to make selections pop up
* you don’t have the same physics constraints
* if there are two items to hold, introduce the user to the most important (needs to be used by dominant hand) of the two first as they are more likely to reach out with their dominant hand
    * this means when they are presented with the second it will have to go into their non-dominant hand

Unity:

* uses metres as distance measure
* change to iso view to align things
* asset store -> steam vr
* steam vr should now be a folder in your assets tab
    * prefabs - bundle of code and shapes
    * move camera rig into the hierarchy
* now when you press play on the screen (and you have the vive plugged in) you can just put your vive on and view it in VR
* VRTK is a good open source toolkit for VR (vive and oculus compatible)
    * good docs online with videos and tutorials
    * full of example scenes you can play around with
    * can take examples, e.g. making objet grabbable, and apply them to your own models or models you purchase on the asset store
* bezier pointer (curved marker thing for teleporting)
* can make changes in realtime (i.e. someone with headset on, other person on computer making the changes)
* unity isn’t for 3D modelling primarily, other programs are better at that, unity is there to give you the realtime capabilities to test out things like physics etc.
* can output a build as an exe, which will be more performant
* this can be passed onto someone with a vive, or even without, to try it out
    * all controls and functionality etc will be built in
* to explore a model, import it into unity and then add in bezier curve control and you can teleport. Export, done

* the player’s head is not the camera. There is no camera in a VR experience. You’ll make them feel sick
* if player needs to move you can block out some peripheral vision to help with sickness (there are other strategies to mitigate this kind of problem)
    * things like static controls (e.g. inside of car) can help if outside is moving
* “friends don’t let friends strafe"
* people move in a straight line at a fairly constant speed (inner ear detects acceleration, but there is none at a constant speed, so there is less chance of inducing nausea)
* avoid acceleration!
* ambient sounds - add room tone for realism
* oculus spatial audio sdk can be imported into unity to give objects sound
* MTP latency - motion to photon latency, time between moving your head and seeing the correct frame
* GPUs for processing with CUDA cores
