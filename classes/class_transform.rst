.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the doc/base/classes.xml source instead.

.. _class_Transform:

Transform
=========

**Category:** Built-In Types

Brief Description
-----------------

3D Transformation.

Member Functions
----------------

+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`Transform<class_Transform_Transform>`  **(** :ref:`Vector3<class_vector3>` x_axis, :ref:`Vector3<class_vector3>` y_axis, :ref:`Vector3<class_vector3>` z_axis, :ref:`Vector3<class_vector3>` origin  **)** |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`Transform<class_Transform_Transform>`  **(** :ref:`Basis<class_basis>` basis, :ref:`Vector3<class_vector3>` origin  **)**                                                                                  |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`Transform<class_Transform_Transform>`  **(** :ref:`Transform2D<class_transform2d>` from  **)**                                                                                                             |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`Transform<class_Transform_Transform>`  **(** :ref:`Quat<class_quat>` from  **)**                                                                                                                           |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`Transform<class_Transform_Transform>`  **(** :ref:`Basis<class_basis>` from  **)**                                                                                                                         |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`affine_inverse<class_Transform_affine_inverse>`  **(** **)**                                                                                                                                               |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`inverse<class_Transform_inverse>`  **(** **)**                                                                                                                                                             |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`looking_at<class_Transform_looking_at>`  **(** :ref:`Vector3<class_vector3>` target, :ref:`Vector3<class_vector3>` up  **)**                                                                               |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`orthonormalized<class_Transform_orthonormalized>`  **(** **)**                                                                                                                                             |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`rotated<class_Transform_rotated>`  **(** :ref:`Vector3<class_vector3>` axis, :ref:`float<class_float>` phi  **)**                                                                                          |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`scaled<class_Transform_scaled>`  **(** :ref:`Vector3<class_vector3>` scale  **)**                                                                                                                          |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform<class_transform>`  | :ref:`translated<class_Transform_translated>`  **(** :ref:`Vector3<class_vector3>` ofs  **)**                                                                                                                    |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| var                                | :ref:`xform<class_Transform_xform>`  **(** var v  **)**                                                                                                                                                          |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| var                                | :ref:`xform_inv<class_Transform_xform_inv>`  **(** var v  **)**                                                                                                                                                  |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Member Variables
----------------

- :ref:`Basis<class_basis>` **basis** - The basis is a matrix containing 3 [Vector3] as its columns: X axis, Y axis, and Z axis. These vectors can be interpreted as the basis vectors of local coordinate system travelling with the object.
- :ref:`Vector3<class_vector3>` **origin** - The origin of the transform. Which is the translation offset.

Description
-----------

Transform is used to store translation, rotation and scaling transformations. It consists of a Basis "basis" and Vector3 "origin". Transform is used to represent transformations of objects in space, and as such, determine their position, orientation and scale. It is similar to a 3x4 matrix.

Member Function Description
---------------------------

.. _class_Transform_Transform:

- :ref:`Transform<class_transform>`  **Transform**  **(** :ref:`Vector3<class_vector3>` x_axis, :ref:`Vector3<class_vector3>` y_axis, :ref:`Vector3<class_vector3>` z_axis, :ref:`Vector3<class_vector3>` origin  **)**

Construct the Transform from four Vector3. Each axis corresponds to local basis vectors (some of which may be scaled).

.. _class_Transform_Transform:

- :ref:`Transform<class_transform>`  **Transform**  **(** :ref:`Basis<class_basis>` basis, :ref:`Vector3<class_vector3>` origin  **)**

Construct the Transform from a Basis and Vector3.

.. _class_Transform_Transform:

- :ref:`Transform<class_transform>`  **Transform**  **(** :ref:`Transform2D<class_transform2d>` from  **)**

Construct the Transform from a Transform2D.

.. _class_Transform_Transform:

- :ref:`Transform<class_transform>`  **Transform**  **(** :ref:`Quat<class_quat>` from  **)**

Construct the Transform from a Quat. The origin will be Vector3(0, 0, 0).

.. _class_Transform_Transform:

- :ref:`Transform<class_transform>`  **Transform**  **(** :ref:`Basis<class_basis>` from  **)**

Construct the Transform from a Basis. The origin will be Vector3(0, 0, 0).

.. _class_Transform_affine_inverse:

- :ref:`Transform<class_transform>`  **affine_inverse**  **(** **)**

Returns the inverse of the transfrom, under the assumption that the transformation is composed of rotation, scaling and translation.

.. _class_Transform_inverse:

- :ref:`Transform<class_transform>`  **inverse**  **(** **)**

Returns the inverse of the transform, under the assumption that the transformation is composed of rotation and translation (no scaling).

.. _class_Transform_looking_at:

- :ref:`Transform<class_transform>`  **looking_at**  **(** :ref:`Vector3<class_vector3>` target, :ref:`Vector3<class_vector3>` up  **)**

Rotate the transform around the up vector to face the target.

.. _class_Transform_orthonormalized:

- :ref:`Transform<class_transform>`  **orthonormalized**  **(** **)**

Returns a transfrom with the basis orthogonal (90 degrees), and normalized axis vectors.

.. _class_Transform_rotated:

- :ref:`Transform<class_transform>`  **rotated**  **(** :ref:`Vector3<class_vector3>` axis, :ref:`float<class_float>` phi  **)**

Rotate the transform around given axis by phi. The axis must be a normalized vector.

.. _class_Transform_scaled:

- :ref:`Transform<class_transform>`  **scaled**  **(** :ref:`Vector3<class_vector3>` scale  **)**

Scale the transform by the specified 3D scaling factors.

.. _class_Transform_translated:

- :ref:`Transform<class_transform>`  **translated**  **(** :ref:`Vector3<class_vector3>` ofs  **)**

Translate the transform by the specified displacement.

.. _class_Transform_xform:

- var  **xform**  **(** var v  **)**

Transforms the given vector "v" by this transform.

.. _class_Transform_xform_inv:

- var  **xform_inv**  **(** var v  **)**

Inverse-transforms vector "v" by this transform.


