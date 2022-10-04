# TwinXR: Twinbase for Indsutrial XR Use Cases

TwinXR is a method we developed to explore the synergies between Digital Twins (DT) and Extened Reality (XR), and their interoperability and interchangeabilty, by introducing an ontology-based approach in industrial Extended Reality (XR) applications. (Related publication is coming out, and we will add the link here.) 

This project creates a customized Twinbase based on the template from the [twinbase/twinbase](https://github.com/twinbase/twinbase) page. This Twinbase includes two twins (Digital Twin documents) of one Univeral Robot UR5e and two overhead cranes: one for the ["Imatar"](https://github.com/Plan-T42/TwinXR-TwinBase-for-HoloCrane/tree/main/docs/9239c7e4-8f96-449a-8f34-3e2d84cea4ff) crane at Aalto Industrial Internet Campus ([AIIC](https://www.aalto.fi/en/industrial-internet-campus/ilmatar-open-innovation-environment)), and the other for a [demo crane](https://github.com/Plan-T42/TwinXR-TwinBase-for-HoloCrane/tree/main/docs/d5657f92-ee00-4ca6-b124-f7b4261d87d4). 

This Twinbase and the DT documents defined here are assessed and utilized by Unity-based HoloLens mixed reality applications for operating robot arm in the project "TwinXR: HoloRobot Unity Demo" (Working In Progress) and cranes in the ["TwinXR: HoloCrane Unity Demo"](https://github.com/Plan-T42/TwinXR-HoloCrane-Unity-Demo) project. Together, they demostrate the use of the "TwinXR" method in industrial applications.

The following content is from the [twinbase/twinbase](https://github.com/twinbase/twinbase) page. 


## Twinbase

Twinbase is an open source platform for managing and distributing [digital twin documents](https://doi.org/10.1109/ACCESS.2020.3045856).
It is built on git and can be hosted on free-of-charge GitHub services.
See an example server live at [dtw.twinbase.org](https://dtw.twinbase.org).

Twinbase is at __*initial development*__ phase and backwards incompatible changes are expected frequently.
Update mechanisms are not yet implemented.

Twinbase is hosted by Aalto University where its development was initiated as a result of the experience from multiple digital twin related projects.
Twinbase is used as a tool for building the Digital Twin Web introduced in Section III of [this article](https://doi.org/10.1109/ACCESS.2020.3045856).
Experiences with Twinbase are used to develop further versions of the [digital twin document standard](https://github.com/AaltoIIC/dt-document).

## Using Twinbase

You can browse the web interface of this Twinbase from the URL shown on the `baseurl` field in the [/docs/index.yaml](/docs/index.yaml) file if this Twinbase is properly configured.

You can fetch twin documents in Python with the [dtweb-python](https://github.com/juusoautiosalo/dtweb-python) library. Available as `dtweb` from pip.

## To create your own Twinbase

1. Create a new repository with the "Use this template" button on the [twinbase/twinbase](https://github.com/twinbase/twinbase) page. (Sign in to GitHub if you can't see the button.)
2. In the newly created repository, activate GitHub Actions from the Actions tab if necessary, and manually run the "File modifier" workflow. (This will modify the files to match your GitHub account. Running the workflow several times will not cause any harm.)
3. Activate GitHub Pages from Settings > Pages > Source to `main` branch and `/docs` folder.
4. A link to Twinbase will be shown at the Pages page. If you have not made any domain customizations, it is in the form \<username\>.github.io/\<repository name\>.
5. Unfortunately any updates from the template repository must be made manually. But you can also just make another Twinbase and copy your twin folders and files there.

Forks can be used as well and might make updating easier, but their use has not been properly tested.

### Creating new twins to your Twinbase

Recommended method to create new twins is to use the new-twin page found on the front page of each Twinbase.

After creating a twin, you need to activate its DT identifier with one of these methods: 
   - To activate the automatically generated dtid.org identifier, send the values of dt-id and hosting-iri of each twin to [this form](https://dtid.org/form).
   - Or you can overwrite the dt-id with the URL given by any [URL shortener service](https://en.wikipedia.org/wiki/URL_shortening#Services) or the [perma-id](https://github.com/perma-id/w3id.org) service. The URL needs to redirect to the hosting-iri.

## To start developing Twinbase

Contribution guidelines are not yet established, but useful contributions are welcome! For development, you can try this:
1. Create your own Twinbase using the Template.
2. Modify your Twinbase as you wish in GitHub.
3. Fork [twinbase/twinbase](https://github.com/twinbase/twinbase). (Do not activate Actions to avoid unnecessary commits.)
4. Manually copy the useful modifications from the repository created with the Template.
5. Submit a pull request.

Local development is a bit tricky as Twinbase uses GitHub Actions as an intergal part of the platform, but feel free to try!

## Support

There are currently no official support mechanisms for Twinbase, but [Juuso](https://juu.so) may be able to help.

## Thanks

Twinbase uses
- [mini.css](https://minicss.org/) to stylize web pages and 
- [json-view](https://github.com/pgrabovets/json-view) to display digital twin documents.

Thanks to the developers for the nice pieces of software!
