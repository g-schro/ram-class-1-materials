Reliability Availability and Maintainability:<br />Theory and Practice on STM32<br /><br />Course Materials
======================================================================================================

This repo contains course materials for the YouTube course 
Reliability, Availability, and Maintainability: Theory and Practice on STM32.

This course consists of seven videos. The YouTube URL is:

https://www.youtube.com/playlist?list=PL4cGeWgaBTe2fGvSVwdYG2F2bxJ2euw8T

This repo contains doucments, and the STM32CubeIDE project files.
Instructions on how to import the project into STM32CubeIDE are below.

There is another repo containing the main code for this course. The URL for
that one is.

https://github.com/g-schro/ram-class-1-code

## STM32CubeIDE Project Files

A zip file of the STM32CubeIDE project `ram-class-nucleo-f401re.zip` is
[here](stm32cubeide/ram-class-nucleo-f401re.zip).  This is valid for
NUCLEO-F401RE board only.

Importing this into STM32CubeIDE:

1. Unzip `ram-class-nucleo-f401re.zip`, possibly into your STM32CubeIDE
   workspace directory (doesn't have to be there). This will create a
   `ram-class-nucleo-f401re` folder.
1. Now go to the STM32CubeIDE GUI.
1. Under the `File` menu, select `Import...`
1. In the `Import` window, select the import wizard: `General`,
   `Existing Projects into Workspace`,
   and click `Next`.
1. Choose `Select root directory`, click `Browse`, find the
   `ram-class-nucleo-f401re` folder, highlight it, and click `Select Folder`.
1. Click `Finish`.

The STM32CubeIDE workspace doesn't contain the main code for the course. That
code is contained in a different GitHub repo (see above). There are different
ways to incorporate this repo code in the STM32CubeIDE project. The way I do it
is by linking to it in using STM32CubeIDE. Here are instructions to do this:

1. Clone the GitHub code repo onto your development system.
1. Now go to the STM32CubeIDE GUI for the `ram-class-nucleo-f401re` project.
1. Go to into the project properties (e.g. using the `Project` menu, and then
   choosing `Properties`).
1. In the `Properties for ram-class-nucleo-f401re` windows, open the
   `C/C++ General` area, and click on `Paths and Symbols`.
1. In the `Paths and Symbols` pane, click the `Source Location` tab, and add two
   folders using the `Link Folder...` button.
    * Name the first folder `Modules`, check the
      `Link to folder in the file system` box, and then click `Browse` and
      select the `modules` folder in the GitHub code repo. Click `Select Folder`
      and then `OK`
    * Name the second folder `App`, check the `Link to folder in the file system`
      box, and then click `Browse` and select the `app1` folder in the GitHub
      code repo. Click `Select Folder` and then `OK`
1. Now `Apply and Close` the `Properties for ram-class-nucleo-f401re` window.

You should be able to build the project now.

## Documents

Below are documents used in the course.

### ARM v7-M Architecture Reference Manual

[Local copy of document version used in vidoes](external-docs/DDI0403E_e_armv7m_arm.pdf)

[External link](https://developer.arm.com/documentation/ddi0403/latest/)

### STM32F401RE Reference manual: RM0368

[Local copy of document version used in developing the course](external-docs/dm00096844-stm32f401xb-c-and-stm32f401xd-e-advanced-arm-based-32-bit-mcus-stmicroelectronics.pdf)

[External link](https://www.st.com/resource/en/reference_manual/dm00096844-stm32f401xb-c-and-stm32f401xd-e-advanced-arm-based-32-bit-mcus-stmicroelectronics.pdf)
