=========================================
Libc++ 14.0.0 (In-Progress) Release Notes
=========================================

.. contents::
   :local:
   :depth: 2

Written by the `Libc++ Team <https://libcxx.llvm.org>`_

.. warning::

   These are in-progress notes for the upcoming libc++ 14 release.
   Release notes for previous releases can be found on
   `the Download Page <https://releases.llvm.org/download.html>`_.

Introduction
============

This document contains the release notes for the libc++ C++ Standard Library,
part of the LLVM Compiler Infrastructure, release 14.0.0. Here we describe the
status of libc++ in some detail, including major improvements from the previous
release and new feature work. For the general LLVM release notes, see `the LLVM
documentation <https://llvm.org/docs/ReleaseNotes.html>`_. All LLVM releases may
be downloaded from the `LLVM releases web site <https://llvm.org/releases/>`_.

For more information about libc++, please see the `Libc++ Web Site
<https://libcxx.llvm.org>`_ or the `LLVM Web Site <https://llvm.org>`_.

Note that if you are reading this file from a Git checkout or the
main Libc++ web page, this document applies to the *next* release, not
the current one. To see the release notes for a specific release, please
see the `releases page <https://llvm.org/releases/>`_.

What's New in Libc++ 14.0.0?
============================

New Features
------------

- There's initial support for the C++20 header ``<format>``. The implementation
  is incomplete. Some functions are known to be inefficient; both in memory
  usage and performance. The implementation is considered experimental and isn't
  considered ABI stable.
- There's a new CMake option ``LIBCXX_ENABLE_UNICODE`` to disable Unicode
  support in the ``<format>`` header. This only affects the estimation of the
  output width of the format functions.

API Changes
-----------

- ...

Build System Changes
--------------------

- Building the libc++ shared or static library requires a C++ 20 capable compiler.
  Use ``-DLLVM_ENABLE_PROJECTS='clang;compiler-rt' -DLLVM_ENABLE_RUNTIMES='libcxx;libcxxabi'``
  to build libc++ using a fresh build of Clang.
