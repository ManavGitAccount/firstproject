# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimal IntelliJ IDEA Java project using Java 26 with preview features enabled. It consists of a single unnamed class (`src/Main.java`) using the Java 21+ unnamed class and simplified entry-point preview APIs (JEP 463).

## Build & Run

This project is managed entirely by IntelliJ IDEA — there is no build tool (Maven/Gradle). Compilation output goes to `out/production/firstproject/`.

**Compile from CLI:**
```
javac --enable-preview --release 26 -d out/production/firstproject src/Main.java
```

**Run from CLI:**
```
java --enable-preview -cp out/production/firstproject Main
```

## Language Features in Use

- **Unnamed classes** (JEP 463/476): `src/Main.java` has no `class` declaration — the file itself is the class.
- **Simplified `main`**: `void main()` with no `String[] args` parameter.
- **`IO.println`**: Preview API (Java 23+) as a shorthand for `System.out.println`. Requires `--enable-preview` at both compile and runtime.
