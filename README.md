Support plane analysis (Lakowicz 2006 section 4.10.3 p. 134) is a rigorous way of assessing parameter uncertainty in decay curve fitting. It is very tedious to do manually, yet to my knowledge no mainstream fluorescence lifetime software to date has a feature to automate it.

The snapshot jar file contains the FLIMJ plugin with support plane analysis feature added by Google Antigravity. Built using an x64 PC running Windows 11, the latest version of Fiji as of 29 July 2026, and the version of FLIMJ cloned from GitHub on 11 September 2026.

To use it in Fiji, first make a backup of the original flimj-ui jar file and then download the jar file from this fork into the jars folder under the Fiji folder.

Instructions given by Yangchen Lin to Antigravity:

***
Clone https://github.com/flimlib/flimj-ui/. This is the FLIMJ plugin in Fiji (ImageJ), which fits fluorescence lifetime decay curves. Implement a new feature in this plugin as follows:
1. Extract the fitted parameter values produced by the plugin from a decay curve fit.
2. For one parameter at a time, change the value slightly from the fitted value and refit the decay curve with that parameter held fixed at the new value.
3. Repeat step 2 for different values of each parameter below and above the original fitted value, and for all parameters.
4. Generate a csv file containing all the results and provide a save button for saving the csv. 
5. Call this new feature "Support Plane Analysis"and attribute it to "Lakowicz 2006 Section 4.10.3 p. 134".
***

After Antigravity submitted the first implementation plan, this modification was requested:

***
Modify the generated CSV structure so that for each target parameter, the original fitted value of that parameter is also included in the set of fixed values for that parameter.
***

The first iteration jar was created from the above instructions and has not been tested manually by humans yet.

After exporting the csv, you can use it to plot the support planes using your favourite software.

Acknowledgements

Timothée Levilly gave guidance on the use of AI.
