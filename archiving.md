# Archiving Policy

## Vinay Setty

### vsetty@acm.org

### Goals

The main goals of this archiving policy are: (i) making sure that the research work
does not get lost and (ii) making sure that we can reproduce the experimental results
contained in publications and share the software that produced them.

### Archive manager (AM)

Vinay Setty (vsetty@acm.org)

## 1 When to archive

It is good practice to start archiving directly after submitting the camera-ready version
of your paper. The ideal workflow looks as follows:

1. Paper accepted and camera-ready version submitted
    - archive the sources of the paper incl. software, experiments, etc.
2. Paper presented
    - archive the sources of the presentation
    - if applicable, archive the conference participation report
3. Software project completed
    - archive the sources of the complete project along with example data
    - add a readme.txt file with (i) an explanation of how to run the software, (ii)
       a rough description of the architecture of the project so that it is easier for
       someone to understand the code and how the classes relate to each other, and
       (iii) a list of papers that this software was used for. Many PhD students extend a system iteratively and build upon a previous version for the next paper.
As the changes might have an influence on the runtimes, each paper still needs to be archived along
with its own copy of the source code (no references to other folders).
4. PhD thesis completed
    - make sure everything concerning the thesis is archived

Note that there is some redundancy in the archiving policy, i.e., the same (or similar)
code might be archived multiple times for different papers: this is acceptable. The only
difference to this rule are big datasets: in such a case, please talk to your supervisor and
the AM.




## 2 Where to archive

/home/prosjekt/deepnews/archive on linux cluster (badne5.ux.uis.no) accessible from any *.ux.uis.no

You need to upload everything under the folder with your username (/home/prosjekt/deepnews/archive/<yourusername>). If the folder for your username does not yet exist, contact the AM.

## 3 What to archive

It is always good practice to make sure that you have submitted the latest versions of
your material to SVN, Git, or whatever else you are using.
For each archive item (paper, thesis, etc.) create areadme.txtfile explaining general
information about the paper. Whenever necessary, create a separatereadme.txtfile for
the subfolders mentioned in the following (software, datasets, etc.) – see also Section 4.

### 3.1 Papers

For each paper, create a separate subfolder in
/home/prosjekt/deepnews/archive/<user>/papers/<newPaper> and archive the follow-
ing items (each in a separate subfolder with the indicated name):

- paper
    the (latex) sources of the camera-ready version of the publication incl. a
    readme.txt file describing how to create the figures in the paper based on the
    obtained experimental results
       - This requires one zip file with the latex code named after the conference and
          year, e.g., ICTIR2019.zip, plus the final pdf of the paper following the same
          naming principle, e.g., ICTIR2019.pdf.
       - A simple reference to a git or SVN repository is not acceptable – listing
          the reference incl. revision number in an accompanying readme.txt file is
          mandatory though.
       - The sources include the compilable latex code that produced the camera-
          ready version of the paper, i.e., the published version of the paper can be
          recreated by compiling the code.
       - The zip file also needs to contain editable source files for the figures, i.e., you
          can include a visio file if that is what you used to create the figures. It is
          not acceptable to reference an online document, e.g., a document on Google
          Drive, etc. The readme.txt file needs to clearly state which program was
          used.
- software
    the software that you used to run the experiments for the paper incl. a readme.txt
    file explaining in detail (list of commands) how to run teh software



- One/multiple file(s) (zip) with all sources (not just executables or package
    file formats such as jars) required to compile and run the software. Providing
    an additional executable binary is strongly encouraged. One readme.txt file
    with
       ∗link to the corresponding git or SVN repository incl. revision number
       ∗programming language
       ∗a description of the general architecture and files
       ∗original test enviroment (Windows, Linux,...)
       ∗dependencies on installed software and environment
       ∗instructions how to compile and run the code incl. example commands,
          etc.
- datasets
datasets used to run the experiments and/or created by the developed software –
along with a description of where the original data was obtained from
- One file (zip) for each dataset. One readme.txt file with a description of the
datasets and instructions on how to use them, how they were created, where
they were downloaded from, general characteristics (size, schema,...), etc.
- If you changed an original dataset, you need to archive both versions: original
and the one you used for the experiments along with a description of how the
original dataset was altered (and the corresponding software)
- experiments
experimental results, incl. the measures you have taken during the experiments
(log files, etc.), expalanation of which figures in the paper correspond to which
log files, how to create these figures from the measures, how to run each of the
experiments in the paper (best: list of commands – make sure to mention which
datasets (file names) were used for which experiment), etc.
- opponents/baselines
the sources of the baseline systems that you compared against incl. a descrip-
tion of how to run them (a description of how to they were run/tuned for the
experiments should be given under “experiments”)
- presentation
sources of the slides of the presentation
- One file (ppt, zip in case of latex beamer, etc.) and one pdf for presentations
at conferences, workshop, seminars, etc.
- As for papers, the editable sources of the used figures need to be archived as
well.
- poster(if applicable – sources of the poster used to present the work),
- coAuthorStatement(if applicable – with signatures),
- conferenceParticipationReport(if applicable),
- anything else that was relevant for the paper.

The name of the paper folder<newPaper>should follow the following naming scheme:
conference name + year + last name of the first author
For example:ICTIR2019setty


### 3.2 Thesis

For your thesis, create a separate subfolder in
/home/prosjekt/deepnews/archive/<user>/<userThesis> and archive the following items
(each in a separate subfolder with the indicated name):

- thesis(latex sources),
- coAuthorStatements(the co-author statements of all papers that are part of the
    thesis),
- presentation(sources of the slides of the presentation at the defense),
- If applicable: a readme.txt file with a description of the evolution of the soft-
    ware and datasets. For instance, which paper builds upon another, which paper
    extends/improves the software/datasets of a previoues one, etc.
- anything else that was relevant for the thesis.

For each of these items follow the instructions stated above in the context of papers.

The name of the folder<userThesis>should follow the following naming scheme:
year + last name of the author
For example:2019setty

## 4 How to archive

In general:

- The zip files should extract the contained files into a subfolder.
- If something you archive is already available in SVN, GIT, etc., then you should
    add the link to the repository to the corresponding readme.txt file. However, ref-
    erencing remote documents/repositories only is not acceptable: everything needs
    to be stored directly in the archive.
- If the data you were using is protected and you are not allowed to share it with
    others, then nevertheless add a description of the dataset to the readme.txt file, add
    some information on where you obtained the dataset from and who is responsible
    for it, and talk to your supervisor and the AM.
- If you use very large datasets (especially in cases where they are used for mul-
    tiple papers), then the dataset should be stored in a special folder (/home/prosjekt/deepnews/archive/<user>/datasets/) and the readme.txt should clearly de-
    scribe the dataset characteristics and state the name of the folder containing it.
    Before using this option, however, please talk to your supervisor and the AM.
- Although this guide mentions .zip archives, you can use appropriate alternative
    archive formats as well, e.g., .tar.gz. If you want to use other formats, please talk
    to your supervisor and the AM.

For tof you not very familiar with linux commands, the server can also be accessed
via hftp, e.g., using a tool such as FileZilla. A useful linux command for copying a
complete local folder (ICTIR2019setty ein this example) is:
scp -r ICTIR2019setty <unix_user>@badne5.ux.uis.no:/home/prosjekt/deepnews/archive/<user>/papers/


## 5 Publishing and licensing

To make it easier to share the code with other researchers, it is recommended to state
some licenses for software and datasets (talk to your supervisor to decide which one to
take). Standard licenses could be:

- datasets: CC BY 4.0 (Creative Commons Attribution 4.0 International License):
    https://creativecommons.org/licenses/by/4.0/
- software: Apache 2.0:https://www.apache.org/licenses/LICENSE-2.
    or
    GPL v3+ (GNU General Public License): https://www.gnu.org/licenses/
    gpl-3.0.html
    At the bottom of this website, there is a section on “how to apply these terms to
    your new programs”, i.e., you need to add a copyright statement to your source
    files.

Note that when publishing the code on a website, we also need to indicate the license
information.


