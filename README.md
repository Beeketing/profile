profile
=======

Simple profiling support package for Go

installation
------------

    go get github.com/davecheney/profile

usage
-----

Enabling profiling in your application is as simple as one line at the top of your main function

    import "github.com/davecheney/profile"

    func main() {
         defer profile.Start(profile.CPUProfile).Stop()
         ...
    }

options
-------

What to profile is controlled by the \*profile.Config value passed to profile.Start. A nil
Config is the same as choosing all the defaults. By default no profiles are enabled.

Several convenience package level values are provided for cpu, memory, and block (contention) profiling. 

For more complex options, consult the documentation on the profile.Config type.
