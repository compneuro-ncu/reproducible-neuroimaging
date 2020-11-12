===============
Data sharing 
===============

Reporting details about your scientific methods is no longer sufficient to address 
the complex relationship between science and society. 
More and more funding bodies require scientists to make their data public after the end of the study. 
Sharing data in open repositories enables other scientists to reuse your data to answer their research question 
or to develop new analysis techniques. 
As a result, society could benefit as much as possible from carrying every single scientific project. 

Optimism about propagating reproducible science is challenged by the complex ethical, 
legal, and social issues it raises. 
Here, we list some conditions you have to fulfill before putting your neuroimaging data into a public repository. 


Ethical approval
-----------------

In case you want to collect neuroimaging data for your project, you first have to apply for study approval 
from the local ethical committee. 
In the application, you have to include the study protocol, a patient or participant information letter, 
a consent form, and some extra information. 

If you plan to share your data in a **public repository**, 
you must write this explicitly in your application to the ethical board. 
Moreover, you have to include the additional consent form, 
where study participants agree to share their data publicly.  

We encourage every researcher to use the `ultimate consent form template <https://open-brain-consent.readthedocs.io/en/latest/ultimate.html>`_
put together in documentation thank to `Open Brain Consent <https://open-brain-consent.readthedocs.io/en/stable/index.html>`_ project.

Data user agreement 
------------------------

**Data User Agreement** specifies how to deal with subject confidentiality issues when accessing identifiable human data.
Once again, Open Brain Consent provides us a `template <https://open-brain-consent.readthedocs.io/en/stable/gdpr/data_user_agreement.html>`_  for such agreement. 
The researcher signing the agreement obliges to be **the data controller** who determines the purposes for which and how personal data is processed.
Additionally, a Data User Agreement helps the researchers to access the data even outside of Europe.

Anonymization process
---------------------------

The raw neuroimaging data contain the personal data that can be used to identify your study participants 
(data headers, facial/skull structure). 
Thus, before sharing the data in a public repository, 
you have to process your data to ensure proper anonymization.


Open Brain Consent lists a several tools that allow researchers to strip out personal data:

- **to sanitize the headers/filenames**:

    * `DeID <https://www.nitrc.org/projects/de-identification>`_ is a Java program which allows users to remove identifying information in neuroimaging datasets, while still maintaining the association among different data types from the same subject for further studies;
    * `PyDICOM’s deid <https://github.com/pydicom/pydicom>`_ is a Python module intended for basic coding of medical images, which means “cleaning” image headers and pixel data, and integrating with your own functions to replace with anonymous identifiers;

- **to skull stripping**:

    * `BET <https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/BET/UserGuide>`_ is the command-line script which deletes non-brain tissue from an image of the whole head;
    * `FSL <https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FslInstallation>`_ is a comprehensive library of analysis tools for FMRI, MRI and DTI brain imaging data;

- **to faces/dental stripping**:

    * `PyDeface <https://github.com/poldracklab/pydeface>`_ is a tool to remove facial structure from MRI images;
    * `mridefacer <https://github.com/mih/mridefacer>`_ aligns template mask to the input image and it requires FSL and the environment variable FSLDIR to be set accordingly.

.. note:: The researcher is obliged to remove all identifying information before sharing the data for research purposes, including full face photographic images and all comparable images, from human subject scans.

Open data sharing platforms
----------------------------

The 2nd step is a submission to a repository before publishing an article that allows the author to 
indicate to readers and reviewers about the specific location of the collected data. 
The data itself may be used by other research in the future. 

The repositories dedicated to sharing neuroimaging data: 

* `OpenfMRI <http://openfmri.org/>`_ platform dedicated to the free and open sharing of raw magnetic resonance imaging (MRI) datasets; 
* `OpenNeuro <https://openneuro.org/>`_ is a platform which accepts datasets which we can upload via our command-line utility tool.

.. note:: Every database stored to this repository conforms to the BIDS data organization scheme. It is also important that these open data sharing platforms do not accept datasets that have not been defaced for privacy considerations and do not contain consent forms.

Attach a license
----------------------

Data is processed differently by the legal system than creative works, therefore they require special licenses. 

Major scientific institutions recommend using an unrestricted Public Domain license such as **CC0** which has universal 
form and it may be used throughout the world for any kind of content without adaptation to account for laws in different 
jurisdictions. 
See `more information <https://creativecommons.org/share-your-work/public-domain/cc0/>`_.
