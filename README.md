# `dm_robotics`: Libraries, Tools, and Tasks for Robotics Research at DeepMind

## Overview

`dm_robotics` is a collection of libraries, tools, and tasks created and used for robotics research at DeepMind. These components are designed to facilitate research in areas such as manipulation, reinforcement learning, computer vision, and more.

## Package Overview

| Package                       | Summary                                                                 |
|-------------------------------|-------------------------------------------------------------------------|
| [Transformations](py/transformations/README.md)     | Rigid body transformations                                             |
| [Geometry](py/geometry/README.md)                   | Scene and robot geometry primitives                                    |
| [Vision](py/vision/README.md)                       | Visual blob detection and tracking                                     |
| [AgentFlow](py/agentflow/README.md)                 | Reinforcement learning agent composition library                        |
| [Manipulation](py/manipulation/README.md)           | "RGB" object meshes for manipulation tasks                              |
| [MoMa](py/moma/README.md)                           | Manipulation environment definition library for simulated and real robots|
| [Controllers](cpp/controllers/README.md)            | QP-optimization based Cartesian controller                              |
| [Controller Bindings](cpp/controllers_py/README.md) | Python bindings for the controller                                      |
| [Least Squares QP](cpp/least_squares_qp/README.md)  | QP task definition and solver                                          |

## Installation

The `dm_robotics` libraries are distributed on PyPI. You can install them with the following package names:

* `dm_robotics-transformations`
* `dm_robotics-geometry`
* `dm_robotics-vision`
* `dm_robotics-agentflow`
* `dm_robotics-manipulation`
* `dm_robotics-moma`
* `dm_robotics-controllers`

### Supported Python Versions

Python versions 3.8, 3.9, and 3.10 are supported.

## Dependencies

Some packages have specific dependencies:
- `MoMa`, `Manipulation`, and `Controllers` require **MuJoCo**.
- Other packages do not have additional dependencies beyond standard libraries like NumPy.

Refer to the individual packages' documentation for detailed information on their dependencies.

## Building the Libraries

To build and test the libraries, you can use the provided `build.sh` script. This script assumes the following prerequisites:

- [`dm_control`](https://github.com/deepmind/dm_control) is installed.
- `cmake` version >= 3.20.2.
- Python 3.8, 3.9, or 3.10, along with system headers, are installed.
- GCC version 9 or later is installed.
- `numpy` is installed.

The libraries are tested using `tox` for Python code and `cmake` for C++ code. The `distshare` mechanism in `tox` is used to share the built source distribution packages between the different components.

### Build & Test Steps:
1. Ensure all dependencies are installed.
2. Run `build.sh` to compile the C++ components and run the tests.

For more details, refer to the individual package documentation for specific setup and usage instructions.

## License

This project is open-source and is licensed under the [appropriate license](LICENSE).

---

For more information and detailed instructions on each package, please refer to the respective README files linked above.
