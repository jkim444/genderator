# Genderator
This Python package uses the underlying data from the program "gender" by Jorg Michael (described [here](http://www.autohotkey.com/community/viewtopic.php?t=22000)).  It's use is pretty straightforward:

    >>> from genderator.detector import *
    >>> d = Detector()
    >>> d.getGender('Bob') == MALE
    True
    >>> d.getGender('Sally') == FEMALE
    True
    >>> d.getGender('Pauley') == ANDROGYNOUS
    True

I18N is fully supported:

    >>> d.getGender(u'�lfr�n') == FEMALE
    True
    >>> d.getGender(u'\301lfr\372n') == FEMALE
    True


If you have an alterative data file, you can pass that in as an optional argument to the Detector.

Try to avoid creating many Detectors, as each creation means reading in the data file.

# Licenses
The genderator code is distributed under the GPLv3.  The data file nam_dict.txt is released under the GNU Free Documentation License.
