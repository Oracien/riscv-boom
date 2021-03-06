Quick-start
===========

The best way to get started with the BOOM core is to use the `Chipyard project template <https://github.com/ucb-bar/chipyard>`__.
There you will find the main steps to setup your environment, build, and run the BOOM core on a C++ emulator.
Here is a selected set of steps from Chipyards `documentation <https://bar-project-template.readthedocs.io/en/latest/>`__:

.. _quick-start-code:
.. code-block:: bash
    :caption: Quick-Start Code

    # Download the template and setup environment
    git clone https://github.com/ucb-bar/chipyard.git
    cd chipyard
    ./scripts/init-submodules-no-riscv-tools.sh

    # build the toolchain
    ./scripts/build-toolchains.sh riscv-tools

    # add RISCV to env, update PATH and LD_LIBRARY_PATH env vars
    # note: env.sh generated by build-toolchains.sh
    source env.sh

    cd sims/verilator
    make CONFIG=LargeBoomConfig

Note: :numref:`quick-start-code` assumes you don't have riscv-tools toolchain installed.
It will pull and build the toolchain for you.
