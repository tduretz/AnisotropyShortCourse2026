# Anisotropy Short Course 2026

The course takes place at the Goethe University of Frankfurt. It is supervised by Andrea Tommasi and Thibault Duretz, and with the support of Anna Bardroff, Filippo Zarabara and Lara Friedrichs.
This short course receives the support of the Heraeus foundation.

This web page only concerns the modelling part of the course.

|       |   |
| ----------- | ----------- |
| <img src="./images/GU.svg" width=150px>       | <img src="./images/Heraeus_foundation_logo.svg" width=300px>       |

## Before the lecture: Get ready!

Before the course, we kindly ask the participants to:

- install the [Julia](https://julialang.org) programming language together with the [VScodium code editor](https://vscodium.com)
- clone and launch the project
- do a basic exercise on array programming and data visualisation  

Dont worry if you don't get things to work on your own. We will take the time to get everything working in the first days of lecture (*after hours*).

### 1) Setting up Julia and VScodium

In this course we will use two softwares: the [Julia](https://julialang.org) programming language and the [VScodium code editor](https://vscodium.com).

### a) Install Julia

See the guide [here](https://apxml.com/courses/getting-started-julia-programming/chapter-1-introducing-julia-setup-first-steps/installing-julia-on-your-system).

Main steps:
- Get the program [juliaup](https://github.com/JuliaLang/juliaup), this tool allows to you to download and manage Julia versions. The tool `juliaup` is available for most platforms.
- Use juliaup to install a Julia version on your computer 

Some useful video resources about Julia installation and basic usage can be found in that [youtube channel](https://www.youtube.com/watch?v=N_CQQgKEbdc&list=PLHohvTggxulqYC3f1gq5x7UqKDteDhA4-).

### b) Install VScodium

Simply go to the [VScodium webpage](https://vscodium.com), download for your platform, and install.

### c) Install the Julia Language Support

Achtung: this step can only be done successfully if step a (and b) are completed.

- open VScodium
- click on the extensions tab to the left of the VScodium window  <img src="./images/extensions_tab.png" width=30px> 
- seach for Julia, you should find and install the Julia Language Support
<img src="./images/Julia_LS.png" width=250px> 

Now you're ready for cloning the course and launching the project...

### 2) Cloning and launching the project

#### a) Cloning the repository using *git*

Once [Julia](https://julialang.org) and [VScodium code editor](https://vscodium.com) are installed, clone or download this repository from the GitHub web page.
We recommend that you **clone** the repository using *git* software (Windows users may have to install git, Linux/MacOS includes it already. You can test your installation by running `git -v` in the terminal. If git is installed properly, this should return its current version).
If you're not familiar with this workflow, you can read [this](https://www.datacamp.com/tutorial/git-clone-command) or ask help from your favourite AI.

The command line to clone the repository is:

`git clone https://github.com/tduretz/AnisotropyShortCourse2026.git`

This will create a new folder in the current directory. 

#### b) Launching into VScodium and testing

After successful cloning of the repository, you can open it locally on your computer:
- In VScodium: clik `File` > `New Window`.
- In VScodium: select the folder of the course `AnisotropyShortCourse2026` and open it.

Let's start the Julia REPL (terminal) from within VScodium.
Use the file explorer of VScodium, to left of the window, click on the tab: <img src="./images/explorer_tab.png" width=30px> 
and open the file `start_julia.jl`.
Execute the file by pressing the play button located at the top-right of the file tab:

<img src="./images/play_button.png" width=200px> 

This will open the Julia REPL inside VScode. If successful, it will greet you with a warm welcome message.

<img src="./images/welcome.png" width=350px> 

Good! The now it's time to instantiate the Julia project. This step downloads and installs all the necessary Julia packages required for our work. In the Julia REPL, press `]`, this will lead you to the package mode

If successful, you should see this: 

<img src="./images/package_mode.png" width=250px> 

Now, type the following command to finalise the procedure and press enter:

`instantiate`

... you probably have to wait a bit. If some packages fail to precompile, just restart Julia (press `Ctrl + D` in the REPL), restart it, and then it should work.

### 3) The preparatory exercise

Use the file explorer of VScodium, to left of the window, click on the tab: <img src="./images/explorer_tab.png" width=30px> 

Open the [preparatory exercise](./scripts/part0/) located in `./scripts/part0/`, the file is called `ArrayProgramming_stud.ipynb`. This is a notebook file than can be edited inside VScodium, using the Julia kernel that was installed in the previous steps. 

Follow the steps and complete the exercise. The aim of the tutorial is to introduce you to working with arrays and visualising data in one and two dimensions.

There is also a very succint introduction to the use of automa tic differentiation ([`ForwardDiff.jl`](https://github.com/JuliaDiff/ForwardDiff.jl)), see the notebook [`AD_Basics.ipynb`](./scripts/part0/).

## [Part 1: Anisotropic rheology in 2D](./scripts/part1)

The lecture notes are available [here](https://next.hessenbox.de/index.php/s/S9JJ6BRqn6TRrqy).

The exercises scripts are available [there](./scripts/part1). 

*Exercise 1*: Program a basic viscous isotropic constitutive law.

*Exercise 2*: Rotate an isotropic material in a pure shear deformation field, check that the response **does not** depend on the orientation :D (0D) 

 <img src="./images/0D_isotropic.png" width=400px> 

*Exercise 3*: Rotate an *ani*sotropic material in a pure shear deformation field, check that the response **does** depend on the orientation! 

 <img src="./images/0D_anisotropic.png" width=400px> 


*Exercise 4*: Use automatic differentiation to determine the constitutive operator in Cartesian coordinates.

 <img src="./images/0D_constitutive.png" width=400px> 

 *Exercise 5*: Make it viscoelastic! 

 <img src="./images/0D_anisotropic_VE.png" width=400px> 


## [Part 2: Anisotropic mechanics in 2D](./scripts/part2)

The lecture notes are available [here](https://next.hessenbox.de/index.php/s/S9JJ6BRqn6TRrqy).

The exercises scripts are available [there](./scripts/part2). 

*Exercise 1*: Program a visous **isotropic** constitutive law into a 2D mechanical code:

 <img src="./images/2D_isotropic.png" width=400px> 


*Exercise 2*: Program a viscous **anisotropic** constitutive law into a 2D mechanical code:

 <img src="./images/2D_anisotropic.png" width=400px> 

 ## References for viscous anisotropy in Geodynamic modelling

Becker, T. W., & Kawakatsu, H. (2011). On the role of anisotropic viscosity for plate‐scale flow. Geophysical Research Letters, 38(17), L17307.

Christensen, U. R. (1987). Some geodynamical effects of anisotropic viscosity. Geophysical Journal International, 91(3), 711–736.

Duretz, T., Tugend, J., Mohn, G., Schmalholz, S. M. (2025). Symmetry versus asymmetry of rifted margins: The role of mechanical anisotropy. Geology.

de Montserrat, A., Faccenda, M., & Pennacchioni, G. (2021). Extrinsic anisotropy of two‐phase Newtonian aggregates: Fabric characterization
and parameterization. Journal of Geophysical Research: Solid Earth, 126(11), e2021JB022232.

Király, Á., Conrad, C. P., & Hansen, L. N. (2020). Evolving viscous anisotropy in the upper mantle and its geodynamic implications. Geochemistry, Geophysics, Geosystems, 21(10), e2020GC009159.

Liu, D., Puel, S., Becker, T. W., & Moresi, L. (2024). Analytical and numerical models of viscous anisotropy: A toolset to constrain the role of
mechanical anisotropy for regional tectonics and fault loading. Geophysical Journal International, 239(2), 950–963. 

Mameri, L., Tommasi, A., Signorelli, J., & Hassani, R. (2020). Olivine‐induced viscous anisotropy in fossil strike‐slip mantle shear zones and
associated strain localization in the crust. Geophysical Journal International, 224(1), 608–625.

Moresi, L., & Mühlhaus, H.‐B. (2006). Anisotropic viscous models of large‐deformation Mohr–Coulomb failure. Philosophical Magazine,
86(21–22), 3287–3305.

Mühlhaus, H. B., Moresi, L., & Cada, M. (2004a). Emergent anisotropy and flow alignment in viscous. PureandAppliedGeophysics, 161(11–12),
2451–2463. 

Perry‐Houts, J., & Karlstrom, L. (2018). Anisotropic viscosity and time‐evolving lithospheric instabilities due to aligned igneous intrusions.
Geophysical Journal International, 216(2), 794–802.

Pouilloux, L., Kaminski, E., & Labrosse, S. (2007). Anisotropic rheology of a cubic medium and implications for geological materials. Geophysical Journal International, 170(2), 876–885.

Signorelli, J., Hassani, R., Tommasi, A., & Mameri, L. (2021). An effective parameterization of texture‐induced viscous anisotropy in orthotropic
materials with application for modeling geodynamical flows. Journal of Theoretical, Computational and Applied Mechanics, 6737.

Tommasi, A., Knoll, M., Vauchez, A., Signorelli, J. W., Thoraval, C., & Logé, R. (2009). Structural reactivation in plate tectonics controlled by
olivine crystal anisotropy. Nature Geoscience, 2(6), 423–427.

Treagus, S. H. (2003). Viscous anisotropy of two‐phase composites, and applications to rocks and structures. Tectonophysics, 372(3), 121–133.
Geophysical Journal International, 170(2), 876–885

Lev, E., & Hager, B. H. (2008). Rayleigh–Taylor instabilities with anisotropic lithospheric viscosity. GeophysicalJournalInternational, 173(3),
806–814.
 
