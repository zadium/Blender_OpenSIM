# Import and Rigging

Import the mesh you want to rig, scale and move as you like

Make your mesh faced to ``Y-`` , this help you to use mirror bones that need this direction, **armature mirror works only in ``X`` axis**

Apply rotations and scales (all)

## Import Mesh

### Bones

You can use it from the [SL Bento](https://wiki.secondlife.com/wiki/Project_Bento_Resources_and_Information)

We provide blender file to use, it is based on original files above, try to use:

* [Bento Female Armature](../Female_SL_Bento_Fixed.blend)

* [Bento Male Armature](../Female_SL_Bento_Fixed.blend)

### Mirroring

After you downloaded the file to rig, or you created your own mesh, it not nessary to use mirror technic, but I prefer it if it symetric

* Cut in half, delete the ``Right`` side of mesh (mesh not the view) for easy to use when click NUM-PAD-3, in pictures I used to delete the ``Left`` side, I am lazy to make new pictures.

Look at how to cut mesh [Cut For Mirror](../examples/CutForMirror/CutForMirror.md)

![Mirror Mesh](MirrorMesh.png)

* When you are editing armature Enable X-Axies Mirror, if you want to keep same changes in both side of bones.

![Using Mirror On Armature](UsingMirrorOnX.png)

* Add/Move Mirror modifier before Armature modifier using X axis

![Mirror Before Armature](MirrorBeforeArmature.png)

* It is really important if you mirrored your mesh, maybe you need to use full texture, included the oppsite side too, check "Mirror U" in "Mirror Modifire" -> "Data"

![Mirror With Texture Full](MirrorWithTextureFull.png)

* Check used groups vertices names of left side exists even if empty, both Left and Right groups must exists.

* Remove/Delete empty vertices groups that unused, I used addon [Easy Weights](https://studio.blender.org/pipeline/addons/easy_weights) it have menu to delete all unused groups.

![Delete Unused Groups](DeleteUnusedGroups.png)

### Roll

Just a trick to fix, but maybe not work

To fix Roll , click Armature-> Bone Roll-> Recalulate Roll-> Globa ``Y-``

## Export

### Export to OpenSIM

To export to OpenSIM, this fix the direction that opensim need it:

* Use Forward = ``X-`` as direction, Up = ``Z``

![Rig Export](RigExportPage01.png)

### Import in OpenSIM/SL [TODO]

LOD Medium as Above if it Hair

Optional set other LODs (lowers) to zero to save with complex mesh

Physic Cube, Analyse if you like

Include Joins if you want to scale the body, no need it for Hair, Clothes

For Tiny meshes, shift down using ``Z`` Offset about ``-0.3``

### Export Animations

For Export to bvh you can try [bvh_enhanced](https://github.com/zaher/blender_bvh_addon_enhanced) (no not mine, I forked it)

Export it using Forward = ``Z-``, Up =``Y``

## References

[Lod in FS](https://www.firestormviewer.org/lod-and-the-upcoming-firestorm-release-the-what-and-why/)

## See Also

[Cut For Mirror](../examples/CutForMirror/CutForMirror.md)

[Rig and Mirror](../examples/RigMirror/readme.md)
