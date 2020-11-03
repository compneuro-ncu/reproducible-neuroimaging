Data sharing process
==========================

Open data availability makes it possible to verify the accuracy of published findings - publicly available data are exposing fewer statistical errors, (Witchers et al. 2011) - and encourages researchers to conduct innovative analyzes. In our case, the whole process is simplified as neuroimaging uses an entirely digital data generation process. 

Optimism about propaging reproducible science is challenged by the increasingly complex ethical, legal and social issues it raises. Reporting of scientific methods is no longer sufficient to address the complex relationship between science and society.


Ethical Approval
-------------------

If we want to apply for approval from an ethical review board to conduct and share brain imaging data, we have to include the study protocol, a patient or participant information letter, a consent form, and some extra information. 

Thus, the 1st step is to **plan data sharing**, which is associated with the ethical approval of the respondent before starting the research procedure. Brain imaging data allows singling out individuals, which is a prerequisite to identification because of sensitive personal data so, thus it is safe to consider them as ‘personal data’.

We encourage every researcher to use the developed format put together in documentation thank to `Open Brain Consent <https://open-brain-consent.readthedocs.io/en/stable/index.html>`_ project, which contribute templates possible to insert into existing **consent form** after minor adjustments. To see ultimate consent forms you can use to your research, `go here <https://open-brain-consent.readthedocs.io/en/latest/ultimate.html>`__.


Data User Agreement 
---------------------

Data User Agreement for accessing identifiable human data, specifies how to deal with subject confidentiality issues. Once again, Open Brain Consent allows using the example of such an agreement which is `available here <using the model of such an agreement>`_ in couple translations. The researcher is “nominated” to be **the data controller** who is determining the purposes for which and the means by which personal data is processed.

What’s more, a Data User Agreement helps researchers to have access to the data even outside of Europe.

Anonymization Process
----------------------

There are some tools which allow researchers to strip out ‘personal data’. Open Brain Consent presents couple of solutions such as:

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

Open Data Sharing Platforms
----------------------------

The 2nd step is a submission to a repository before publishing an article allows the author to indicate to readers and reviewers the specific location of the collected data. The data itself may be used for other research in the future. 

There is an widespread repository in the research community accepting data from human neuroimaging: 

* `OpenfMRI <http://openfmri.org/>`_ platform dedicated to the free and open sharing of raw magnetic resonance imaging (MRI) datasets; 
* `OpenNeuro <https://openneuro.org/>`_ is a platform which accepts datasets which we can upload via our command-line utility tool.

.. note:: Every database stored to this repository conforms to the BIDS data organization scheme. It is also important that these open data sharing platforms do not accept datasets that have not been defaced for privacy considerations and do not contain consent forms.

Attach a License
----------------------

Data is processed differently by the legal system than creative works, therefore they require special licenses. 

Major scientific institutions recommend using an unrestricted Public Domain license such as **CC0** which has universal form and it may be used throughout the world for any kind of content without adaptation to account for laws in different jurisdictions. To see more information, `click here <https://creativecommons.org/share-your-work/public-domain/cc0/>`__.
