.. |date| date::

Create and manage volumes
=========================

Last changed: |date|

.. contents::


Volumes are block storage devices that you attach to instances to
enable persistent storage. You can attach a volume to a running
instance or detach a volume and attach it to another instance at any
time. You can also create a snapshot from or delete a volume.


Create a volume
---------------

In the dashboard, select **Volumes** in the **Compute** tab:

.. image:: images/dashboard-volumes-01.png
   :align: center
   :alt: Dashboard - Compute -> Volumes

Click on ``Create Volume``, and the following window appears:

.. image:: images/dashboard-create-volume-01.png
   :align: center
   :alt: Dashboard - Create Volume

Fill in the form:

* **Volume Name**: A name for the volume, which you will recognize
  (Required)
* **Description**: An optional description
* **Volume Source**: Either no source, i.e. an empty volume, or create
  a volume from an image
* **Type**: Choose "rbd"
* **Size**: The size of the volume, in GB
* **Availability Zone**: Choose "nova"

Then click ``Create Volume``. The volume will be instantly created and
available:

.. image:: images/dashboard-create-volume-02.png
   :align: center
   :alt: Dashboard - Create Volume finished


Attach a volume to a virtual machine
------------------------------------

After creating one or more volumes, you can attach them to virtual
machine (instances). A volume is a block storage device, and can only
be attached to one virtual machine at a time. In the **Volumes** tab
under **Compute**, select *Manage Attachments* from the dropdown menu:

.. image:: images/dashboard-attach-volume-01.png
   :align: center
   :alt: Dashboard - Attach volume

Select the virtual machine (instance) that you wish to attach this
volume to. You usually don't need to change the device name. Then
click on ``Attach Volume``.

.. image:: images/dashboard-attach-volume-02.png
   :align: center
   :alt: Dashboard - Attach volume

The volume is now attached to the virtual machine.


Detach a volume from a virtual machine
--------------------------------------

In order to detach a volume from a virtual machine (instance),
select *Manage Attachments* from the dropdown menu in the **Volumes** tab
under **Compute**:

.. image:: images/dashboard-detach-volume-01.png
   :align: center
   :alt: Dashboard - Detach volume

Select the attachment and click on ``Detach Volume``:

.. image:: images/dashboard-detach-volume-02.png
   :align: center
   :alt: Dashboard - Detach volume part 2

You will have to confirm this action. Click ``Detach Volume`` in the
confirmation dialog that appears:

.. image:: images/dashboard-detach-volume-03.png
   :align: center
   :alt: Dashboard - Detach volume confirmation

The volume is now detached.


Delete a volume
---------------
