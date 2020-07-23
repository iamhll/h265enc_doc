.. -----------------------------------------------------------------------------
  ..
  ..  Filename       : main.rst
  ..  Author         : Huang Leilei
  ..  Created        : 2020-07-23
  ..  Description    : introduction related documents
  ..
.. -----------------------------------------------------------------------------

Introduction
============

Project Tree
------------

current tree
............

::

    .
    ├── branch
    │   ├── HighSpeedVersion
    │   ├── chgu
    │   ├── h265_v2019
    │   ├── hll
    │   ├── liwei
    │   ├── tang
    │   └── yheng
    ├── tag
    │   ├── open-version
    │   └── open-version-2
    └── trunk
        ├── doc
        ├── include
        ├── lib
        ├── ref
        ├── rtl
        ├── sim
        └── syn


targeted tree
.............

::

    .
    ├── doc
    ├── ext
    │   ├── HighSpeedVersion
    │   ├── ...
    │   └── ...
    ├── include
    ├── lib
    ├── lint
    ├── ref
    ├── rtl
    │   ├── enc
    │   │   ├── enc_core
    │   │   │   ├── enc_fth
    │   │   │   ├── enc_rmd
    │   │   │   ├── enc_ime
    │   │   │   ├── enc_fme
    │   │   │   ├── enc_rdo
    │   │   │   ├── enc_ilf
    │   │   │   ├── enc_e_c
    │   │   │   ├── enc_dmp
    │   │   │   ├── enc_buf
    │   │   │   └── enc_core_top.v
    │   │   ├── enc_itf
    │   │   ├── enc_mem
    │   │   └── enc_top.v
    │   ├── dec
    │   │   └── dec_core
    │   │       └── dec_e_d
    │   └── common
    ├── script
    ├── sim
    └── syn


Macro-Definition List
---------------------

.. table::
    :align: left
    :widths: auto

    ======== ====== =============
     Domain   Name   Description
    ======== ====== =============
    ======== ====== =============


Parameter List
--------------

.. table::
    :align: left
    :widths: auto

    ======== ====== =============
     Domain   Name   Description
    ======== ====== =============
    ======== ====== =============


Owner
-----

.. table::
    :align: left
    :widths: auto

    ================================= ===========================
     Directory                         Owner
    ================================= ===========================
     doc/                              ...
     ext/HighSpeedVersion              Huang Leilei
     include                           Huang Leilei
     lib                               Huang Leilei
     lint                              Huang Leilei
     ref                               Huang Leilei
     rtl/enc/                          Huang Leilei
     rtl/enc/enc_core/enc_fth/         Shi Chunxin, Li Tingting
     rtl/enc/enc_core/enc_r_c/         Hao Zhijian
     rtl/enc/enc_core/enc_rmd/         Huang Leilei
     rtl/enc/enc_core/enc_ime/         Huang Leilei, Shi Chunxin
     rtl/enc/enc_core/enc_fme/         Huang Leilei
     rtl/enc/enc_core/enc_rdo/         Huang Leilei, Liu Xun
     rtl/enc/enc_core/enc_ilf/         Liu Xun, Hou Bingjing
     rtl/enc/enc_core/enc_e_c/         Cai Yujie, Zou Yuliang
     rtl/enc/enc_core/enc_dmp/         Huang Leilei
     rtl/enc/enc_core/enc_buf/         Huang Leilei
     rtl/enc/enc_core/enc_core_top.v   Huang Leilei
     rtl/enc/enc_core/enc_itf          Shi Chunxin, Li Tingting
     rtl/enc/enc_core/enc_mem          Huang Leilei
     rtl/enc/enc_top.v                 Huang Leilei
     rtl/dec/dec_core/dec_e_d          Cai Yujie, Zou Yuliang
     rtl/common                        Huang Leilei
     script                            Huang Leilei
     sim                               ...
     syn                               Huang Leilei
    ================================= ===========================


Task List
---------

.. table::
    :align: left
    :widths: auto

    ================= ============= ================================================== ================== =================
       Number            Directory     Task                                               Owner              Status
    ================= ============= ================================================== ================== =================
     **20200727-01**   **/**         **relocate files according to new project tree**   **Huang Leilei**   **Not Started**
     **20200727-02**   **lint/**     **maintain**                                       **Huang Leilei**   **Not Started**
     **20200727-03**   **script/**   **maintain**                                       **Huang Leilei**   **Not Started**
     **20200727-04**   **sim/**      **maintain**                                       **Huang Leilei**   **Not Started**
     **20200727-05**   **syn/**      **maintain**                                       **Huang Leilei**   **Not Started**
     **20200727-06**   **ext/**      **maintain**                                       **Huang Leilei**   **Not Started**
    ================= ============= ================================================== ================== =================
