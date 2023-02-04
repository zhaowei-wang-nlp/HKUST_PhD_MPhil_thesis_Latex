HKUST_PhD/MPhil_thesis_Latex
======================

*This template can also be used in MPhil thesis after changing all "PhD" to "MPhil".*

This is a HKUST PhD/MPhil thesis latex template based on the latest official sample (https://fytgs.hkust.edu.hk/sites/default/files/imce/thesis_sample_page_mphil.pdf)

This repo is forked from https://github.com/fcyu/HKUST_PhD_MPhil_thesis_Latex, with bugs fixed.

I record all the bugs I encountered in my own writing and provide referencing solutions.

1. Cannot insert figures
Solution: The ```\@xfloat``` in the file ```thesis.sty``` is badly defined.
Redefine it as this:
```
\let\my@xfloat\@xfloat
\def\@xfloat#1[#2]{
	\my@xfloat#1[#2]%
	\def\baselinestretch{1}%
	\@normalsize \normalsize
}
```


Please report issues if there is any questions or requirements.

