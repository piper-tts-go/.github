This project is a hard fork of the [Piper](https://github.com/rhasspy/piper) text-to-speech software and a third-party Go module that embeds Piper into Go programs.
I created this fork to solve problems I encountered while developing [SkyEye](https://github.com/dharmab/skyeye):

1. The Piper ecosystem did not have good support for macOS on Apple Silicon:
    1. A bug in Piper's CI/CD workflow caused the macOS build to use the latest macOS runner at build time; the architecture of the runner was not specified. This caused upstream releases of Piper to be built with the wrong CPU architecture on macOS.
    1. The Go module did not support macOS; one of my collaborators on SkyEye had to add support in his soft fork.
1. The Go module did not expose all Piper options; again, my collaborator had to add support in his soft fork.
1. The default voices available for the Go module had Irish and British accents. Some of my users, especially those who speak English as a second language, found these accents difficult to understand. I wanted to provide more options with higher clarity.
1. Both Piper and the Go module's maintainers appear to be inactive and unresponsive to bug reports.

I have hard forked all software mentioned and intend to maintain its existing functionality. However, I am not a domain expert on text-to-speech or AI voice synthesis and do not plan to add significant new features.
