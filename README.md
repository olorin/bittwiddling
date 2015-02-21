# Snippets for bit-twiddling

I find I need to implement certain operations (e.g., endianness
conversions, manipulating bitmasks, et cetera) in most of my C projects.
Many of them (embedded applications in particular) don't make the
prospect of linking in an entire library for a few trivial functions
very appealing. This repository is intended to provide a common location
for such trivial operations, implemented to be reusable,
minimal-overhead, and conducive to use in isolation.

# Usage

Everything is implemented as cpp macros, not C++), so it can be dropped
in as a single header file without introducing overhead from the
functionality you don't use. If you're working in an extremely
low-memory environment it might make sense to use non-inlined
functions over macros, though I've never actually encountered such a
case.

# Licensing

The content of this repository is in the public domain, to facilitate
its intended use (as needed, without worrying about license
compatibility or attribution requirements). This decision was influenced
by the number of times I've had to reimplement solutions which already
exist, but as part of a large library (precluding depending on the whole
thing when I'm writing code for a tiny microcontroller) released under
the GPL (precluding just copying the files I need into my MIT-licensed
projects).
