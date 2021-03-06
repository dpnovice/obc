.. _sec_use_cases:

Use Cases
---------

This section describes use cases for end-user interaction, including:

* use the controls design tool to design a control sequence and export
  it as a CDL-compliant specification,
* use the CDL to bid on a project and, when selected for the project,
  implement the control sequence in a building automation system, and
* use the commissioning and functional verification tool during commissioning.
* Use control design tool to create control diagrams in addition to control sequences 
  and automatically produce a points list with a standard naming convention and/or tagging 
  convention, a plain language SOO, and verification that the control diagram includes 
  all instrumentation required to complete the control sequence.
* Use control design tool during construction to assist the controls integration process by 
  identifying network protocol, communication protocol and points list discrepancies between 
  systems and equipment.   


Controls design
^^^^^^^^^^^^^^^


Customizing a control sequence for a VAV system
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This use case describes how to customize a control sequence
for a VAV system.

===========================  ===================================================
**Use case name**            **Customizing a control sequence for a VAV system**
===========================  ===================================================
Related Requirements         n/a
---------------------------  ---------------------------------------------------
Goal in Context              A mechanical engineer wants to customize a control
                             sequence, starting with a template.
---------------------------  ---------------------------------------------------
Preconditions                HVAC system model connected to building model.

                             Preconfigured control sequence, stored in the
                             OpenBuildingControls library.

                             A set of performance requirements.
---------------------------  ---------------------------------------------------
Successful End Condition     Implemented VAV sequence with customized control,
                             ready for performance assessment
                             (Use case :ref:`use_case_per_ass`) and
                             ready for export in CDL.
---------------------------  ---------------------------------------------------
Failed End Condition         n/a
---------------------------  ---------------------------------------------------
Primary Actors               A mechanical engineer.
---------------------------  ---------------------------------------------------
Secondary Actors             The controls design tool with template control
                             sequences and a package with elementary CDL blocks.

                             The HVAC and controls library.
---------------------------  ---------------------------------------------------
Trigger                      n/a
---------------------------  ---------------------------------------------------
**Main Flow**                **Action**
---------------------------  ---------------------------------------------------
1                            The user opens the controls design tool in OpenStudio
---------------------------  ---------------------------------------------------
2                            The user opens the HVAC model and building model
                             in the controls design tool.
---------------------------  ---------------------------------------------------
3                            The user connects sensors and actuators to
                             control inputs and outputs.
---------------------------  ---------------------------------------------------
4                            The user drags and drops from the Buildings library
                             a pre-configured VAV control sequence.
---------------------------  ---------------------------------------------------
5                            The user clicks on the pre-configured VAV control
                             sequence and selects in the tool a function that
                             will store the sequence in the project library
                             to allow further editing.
---------------------------  ---------------------------------------------------
6                            The controls design tool stores the
                             sequence in the project library.
---------------------------  ---------------------------------------------------
7                            The user opens in the project library
                             the new composite control block.
---------------------------  ---------------------------------------------------
8                            The user adds and connects additional control blocks
                             from the elementary CDL-block library.
---------------------------  ---------------------------------------------------
9                            The user selects "Check model" to verify whether
                             the implemented sequence complies with the CDL
                             specification.
===========================  ===================================================


:numref:`fig_use_case_custom_vav` shows the sequence diagram for this use case.

.. _fig_use_case_custom_vav:

.. uml::
   :caption: Customizing a control sequence for a VAV system.

   title Customizing a control sequence for a VAV system

   "User" -> "OpenStudio" : Open control design tool.
   "OpenStudio" -> "Control Design Tool" : open()
   "User" -> "Control Design Tool" : Open HVAC and building model.
   "OpenStudio" <- "Control Design Tool" : Request HVAC and building model.
   "User" -> "Control Design Tool" : Drag & drop pre-configured control sequence.
   "User" -> "Control Design Tool" : Connect sensors and actuators to control inputs and outputs.
   "User" -> "Control Design Tool" : Select to store the control sequence in the project library.
   "Control Design Tool" -> "Control Design Tool" : Write the sequence to new file in the project library.
   "User" -> "Control Design Tool" : Open new composite control block in the project library.
   "User" -> "Control Design Tool" : Drag, drop and connect blocks from CDL library.
   "User" -> "Control Design Tool" : Check model.
   "OpenStudio" <- "Control Design Tool" : Invoke model check.
   "User" <- "Control Design Tool" : Report info, warning and error.


.. _use_case_per_ass:

Performance assessment of a control sequence
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This use case describes how to assess the peformance of a control sequence
in the controls design tool.

xxx.




Export of the control sequence in CDL
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx

Saving the control sequence in a library for use in future projects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx

Importing a CDL for trouble shooting an existing building
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx


CDL processing for bidding and implementation in building automation system
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Processing the CDL for cost-estimation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx

Processing the CDL for implementation in building automation system using code translation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx

Processing the CDL for implementation in building automation system using manual implementation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx

Commissioning
^^^^^^^^^^^^^

Verification of requirements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx

Conducting functional verification tests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

xxxx
