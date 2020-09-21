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

(20200921) Project Tree
-----------------------

::

    /
    ├── chk                          [not       open] check environments
    ├── doc                          [partially open] documents
    ├── ext                          [partially open] extended features
    ├── include                      [partially open] inlcude files like definitions and parameters
    ├── lib                          [          open] library files like memory models
    ├── ref                          [          open] reference models
    ├── src                          [          open] source codes
    │   ├── common                   [          open] common codes
    │   ├── enc                      [          open] encoder related codes
    │   │   ├── enc_knl              [          open] encoder kernel related codes
    │   │   │   ├── enc_fth          [          open] fetch related codes
    │   │   │   ├── enc_rmd          [          open] rough mode decision related codes
    │   │   │   ├── enc_ime          [          open] integer motion estimation related codes
    │   │   │   ├── enc_fme          [          open] fractional motion estimation related codes
    │   │   │   ├── enc_rdo          [          open] rate-distortion optimization related codes
    │   │   │   ├── enc_ilf          [          open] in-loop filter related codes
    │   │   │   ├── enc_e_c          [          open] entropy encoding related codes
    │   │   │   ├── enc_dmp          [          open] dump related codes
    │   │   │   ├── enc_buf          [          open] buffer related codes
    │   │   │   └── enc_knl_top.v    [          open] top of encoder kernel
    │   │   ├── enc_itf              [          open] interface related codes
    │   │   │   └── enc_rfc          [          open] reference frame compression related codes
    │   │   ├── enc_mem              [          open] memory related codes
    │   │   └── enc_top.v            [          open] top of encoder
    │   └── dec                      [          open] decoder related codes
    │       └── dec_knl              [          open] decoder kernel related codes
    │           └── dec_e_d          [          open] entropy decoding related codes
    ├── script                       [partially open] scripts
    ├── sim                          [          open] simulation environments
    └── syn                          [not       open] synthesis environments


(20200921) Macro-Definition List
--------------------------------

    please check /include/defines_enc.vh


(20200921) Parameter List
-------------------------

    please check /include/parameters_enc.vh


(20200921) Owner
----------------

.. table::
    :align: left
    :widths: auto

    ================================= ===========================
     Directory                         Owner
    ================================= ===========================
     chk/                              Huang Leilei
     doc/                              ...
     ext/                              Huang Leilei
     include/                          Huang Leilei
     lib/                              Huang Leilei
     ref/                              Huang Leilei
     rtl/common                        Huang Leilei
     rtl/enc/                          Huang Leilei
     rtl/enc/enc_knl/enc_fth/          Shi Chunxin, Li Tingting
     rtl/enc/enc_knl/enc_rmd/          Huang Leilei
     rtl/enc/enc_knl/enc_ime/          Huang Leilei, Shi Chunxin
     rtl/enc/enc_knl/enc_fme/          Huang Leilei, Shi Chunxin
     rtl/enc/enc_knl/enc_rdo/          Huang Leilei, Liu Xun
     rtl/enc/enc_knl/enc_ilf/          Liu Xun, Hou Bingjing
     rtl/enc/enc_knl/enc_e_c/          Cai Yujie, Zou Yuliang
     rtl/enc/enc_knl/enc_dmp/          Shi Chunxin, Li Tingting
     rtl/enc/enc_knl/enc_buf/          Huang Leilei
     rtl/enc/enc_knl/enc_knl_top.v     Huang Leilei
     rtl/enc/enc_knl/enc_itf           Shi Chunxin, Li Tingting
     rtl/enc/enc_knl/enc_mem           Huang Leilei
     rtl/enc/enc_top.v                 Huang Leilei
     rtl/dec/dec_knl/dec_e_d           Cai Yujie, Zou Yuliang
     script                            Huang Leilei
     sim                               ...
     syn                               Huang Leilei
    ================================= ===========================


(20200921) Task List
--------------------

gantt

    please check the corresponding one in https://f265enc-doc.readthedocs.io/en/latest/introduction/main.html#task-list

.. table:: **2020.09**
    :align: left
    :widths: auto

    ============= ======================= ======================================================== ============================ ============== =====================
     Number        Task                    Start Point                                              Target Module                Owner          Status
    ============= ======================= ======================================================== ============================ ============== =====================
     20200914-01   synchronize HW and SW   update/rtl/000/syncHwAndSw                               /rtl/enc/enc_core/enc_rmd/   Huang Leilei   20200915 - 20200915
     20200914-01   synchronize HW and SW   update/rtl/000/syncHwAndSw                               /rtl/enc/enc_core/enc_ime/   Huang Leilei   20200916 - 20200916
     20200914-01   synchronize HW and SW   update/rtl/000/syncHwAndSw                               /rtl/enc/enc_core/enc_fme/   Huang Leilei   20200917 - 20200917
     20200914-01   synchronize HW and SW   update/rtl/000/syncHwAndSw                               /rtl/enc/enc_core/enc_rdo/   Huang Leilei   20200918 - 20200918
     20200914-02   optimize                update/rtl/enc/enc_itf/002/furtherOptimize               /rtl/enc/enc_itf/            Shi ChunXin    \* 20200914
     20200914-03   optimize dbf            update/rtl/enc/enc_knl/enc_ilf/001/optimizeCodingStyle   /rtl/enc/enc_knl/enc_ilf/    Liu Xun        \* 20200914
     20200921-01   relocate and rename     master                                                   /                            Huang Leilei   20200921 - 20200921
    ============= ======================= ======================================================== ============================ ============== =====================

\

.. table:: **2020.08**
    :align: left
    :widths: auto

    ============= ========== ============== =============== ============== =====================
     Number        Task       Start Point    Target Module     Owner          Status
    ============= ========== ============== =============== ============== =====================
     ...           ...        master         ...             ...
    ============= ========== ============== =============== ============== =====================

\

.. table:: **2020.07**
    :align: left
    :widths: auto

    ============= ========== ============== =============== ============== =====================
     Number        Task       Start Point    Target Module     Owner          Status
    ============= ========== ============== =============== ============== =====================
     20200725-01   relocate   master         /               Huang Leilei   20200725 - 20200725
     20200725-02   maintain   master         /script/        Huang Leilei   20200725 - 20200725
     20200725-02   maintain   master         /sim/           Huang Leilei   20200725 - 20200725
     20200725-02   maintain   master         /chk/           Huang Leilei   20200725 - 20200725
     20200725-02   maintain   master         /syn/           Huang Leilei   20200725 - 20200725
     20200725-02   maintain   master         /ext/           Huang Leilei   20200725 - 20200725
     ...           ...        master         ...             ...
    ============= ========== ============== =============== ============== =====================
