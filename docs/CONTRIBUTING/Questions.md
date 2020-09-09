# Asking questions

Sometimes you have a general question that you'd like to ask which isn't exactly a bug or a feature request.

In these cases, filing an issue on github isn't generally the best way to do it since questions might turn into a conversation or a discussion and don't have a defined scope.

Instead these questions can be asked in one of RenderDoc's community spaces, such as in [#renderdoc on freenode IRC](https://kiwiirc.com/client/irc.freenode.net/#renderdoc) or on RenderDoc's [Discord server](https://discord.gg/ahq6yRB). If your question is more private you can [email me directly at baldurk@baldurk.org](mailto:baldurk@baldurk.org).

Please note that in all these places RenderDoc's [code of conduct](../CODE_OF_CONDUCT.md) still applies.

hello, I am learning the core abort renderdoc.  I have some problem about hook. 

------------------------------------------------------------------------

struct init
{
  init() { library_loaded(); }
} do_init;

// we want to be sure the constructor and library_loaded are included even when this is in a static
// library, so we have this global function that does nothing but takes the address.
extern "C" __attribute__((visibility("default"))) void *force_include_libentry()
{
  return &do_init;
}
----------------------------------------------------------------- from renderdoc-1.9\renderdoc\os\posix\posix_libentry.cpp

I do not know which function have called "force_include_libentry" ?  Is the game app calling ?

Thanks very much, waiting for your answer.
