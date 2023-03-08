# openai [![crates.io](https://img.shields.io/crates/v/openai.svg)](https://crates.io/crates/openai/) [![Rust workflow](https://github.com/valentinegb/openai/actions/workflows/rust.yml/badge.svg)](https://github.com/valentinegb/openai/actions/workflows/rust.yml)

An unofficial Rust library for the OpenAI API.

> **Note**
>
> The ownership of the `openai` package on crates.io has been transfered to me, Valentine Briese (not the previous owner).
> This is an entirely different project than the one that was on crates.io as `openai` previously!

> **Warning**
> 
> Currently in alpha, I wouldn't recommend using in any production applications.

## Core Principles

- Instead of accessing all functions as methods on a single client-like structure,
  functions should be accessed from their own modules.
- Environmental variables should be the prioitized method of authentication,
  but you shouldn't be forced to do things this way.
- This is a LIBRARY, not a WRAPPER!
  The goal here isn't to just give some basic wrapper functions for making HTTP requests,
  it's to "rust-ify" things. We want to create the illusion that the OpenAI API was made in Rust first!
- What is this, C? No, it's Rust! We follow the object-oriented paradigm, not the procedural one.
  What this mainly means is less `create_completion()`, more `Completion::create()`.
