.. -----------------------------------------------------------------------------
    ..
    ..  Filename       : main.rst
    ..  Author         : Huang Leilei
    ..  Created        : 2020-09-21
    ..  Description    : check list related documents
    ..
.. -----------------------------------------------------------------------------

Check List
==========

(20200921) Major Developments
-----------------------------

    .. table::
        :align: left
        :widths: auto

        +---------+-----------+---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        | Subject | Main Step | Sub Step                                    | Check List                                                                                          |
        +=========+===========+=============================================+=====================================================================================================+
        | manager | assign    | define tasks                                | manager must make tasks clear and as individual as possible                                         |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | define start points                         | manager should creat start points and push them to the remote                                       |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | define target modules, due dates and owners | manager must make target modules, due dates and owners clear and release them with Gantt chart      |
        +---------+-----------+---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        | owner   | execute   | create branch                               | | if multiple owners or modules are involved,                                                       |
        |         |           |                                             | |   owner should create a sub-branch named with start_point/owner/module                            |
        |         |           |                                             | |   (for example, undergoing/update/src/enc/enc_knl/000/optimizeTiming/SCX/rfc)                     |
        |         |           |                                             | | else                                                                                              |
        |         |           |                                             | |   owner could directly works on the start point                                                   |
        |         |           |                                             | |   (for example, undergoing/update/src/enc/enc_knl/enc_rdo/optimizeCost/master                     |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | edit                                        | | owner should divide his edits into atomic ones                                                    |
        |         |           |                                             | | owner should code according to the coding style and template                                      |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | commit                                      | | **owner must avoid dos-format files:**                                                            |
        |         |           |                                             | |   **cd script; ./runListUpdate.sh**                                                               |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | push                                        | | **owner must clean warnings:**                                                                    |
        |         |           |                                             | |   **cd sim/rtl\_???; make com_view**                                                              |
        |         |           |                                             | | owner should pass simulation:                                                                     |
        |         |           |                                             | |   cd sim/rtl\_???; make sim                                                                       |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | feedback                                    | | if one task is finished,                                                                          |
        |         |           |                                             | |   owner should notify the corresponding manager as quick as possible                              |
        |         |           |                                             | | else                                                                                              |
        |         |           |                                             | |   owner should report the percentage of completeness on daily meetings                            |
        +---------+-----------+---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        | manager | verify    | check                                       | manager must rerun compilation and simulation                                                       |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | review                                      | | manager must check the differences with master and point out any violation noticed                |
        |         |           |                                             | | violations include but not limited to                                                             |
        |         |           |                                             | |   dos-format files and tailing blanks                                                             |
        |         |           |                                             | |   improper logic like listing all situations instead of using for-loop                            |
        |         |           |                                             | |   improper coding styles like improper naming, magic numbers                                      |
        |         |           +---------------------------------------------+-----------------------------------------------------------------------------------------------------+
        |         |           | feedback                                    | | if another iteration is needed                                                                    |
        |         |           |                                             | |   manager must note down TODOs, push them to the remote and notify corresponding owners           |
        |         |           |                                             | | else                                                                                              |
        |         |           |                                             | |   manager must merge the branch to master by                                                      |
        |         |           |                                             | |   (G) copying the branch from global tree to local tree                                           |
        |         |           |                                             | |   (L) minimizing differences with master                                                          |
        |         |           |                                             | |   (L) doing more checks with local scripts                                                        |
        |         |           |                                             | |       (if failed, manager should relaunch a new iteration)                                        |
        |         |           |                                             | |   (L) updating the status of corresponding modules in this page                                   |
        |         |           |                                             | |   (L) updating the version number and descriptions in defines_enc.vh                              |
        |         |           |                                             | |   (L) modifying branch prefix from undergoing to merged                                           |
        |         |           |                                             | |   (L) making a shortcut from master to branch and create a tag                                    |
        |         |           |                                             | |   (L) pushing master, the newly-add tag and the newly-merged branch to orgin, aliyun and github   |
        |         |           |                                             | |   (L) copying the branch from local tree back to global tree                                      |
        |         |           |                                             | |   (G) making a shortcut from master to branch and create a tag                                    |
        |         |           |                                             | |   (G) pushing master, the newly-add tag and the newly-merged branch to aliyun                     |
        |         |           |                                             | |   (G) protecting the merged branch on git@code.aliyun.com:llhuang/h265enc_global.git              |
        |         |           |                                             | |   (S) notify all developers about the change on master                                            |
        |         |           |                                             | | (G for global, L for local, S for system)                                                         |
        +---------+-----------+---------------------------------------------+-----------------------------------------------------------------------------------------------------+


(20200922) SRC and SIM Status
-----------------------------

    .. table:: **SRC**
        :align: left
        :widths: auto

        +-------------+------------------+------------------+--------------+
        | Module      | Hardware Version | Software Version | Status       |
        +=============+==================+==================+==============+
        | enc_rmd_top | syn/20200914 + 3 | syn/20200914     | Synchronized |
        +-------------+------------------+------------------+--------------+

    \

    .. table:: **SIM**
        :align: left
        :widths: auto

        +-------------+------------------+-------------+------------------+--------------+
        | Module      | Version          | Check Point | Checker          | Status       |
        +=============+==================+=============+==================+==============+
        | enc_rmd_top | syn/20200914 + 3 | ram_mod_wr  | CHKO_RMD_TOP_MOD | Synchronized |
        +-------------+------------------+-------------+------------------+--------------+

    \


(20200922) Flow Status
----------------------

    .. table:: **check**
        :align: left
        :widths: auto

        +-------------+------------------+---------------+--------------+-----------+-------+--------------------+
        | Module      | Version          | update script | check script | NCverilog | Verdi | Spyglass           |
        +=============+==================+===============+==============+===========+=======+====================+
        | enc_rmd_top | syn/20200914 + 3 | pass          | pass         | pass      | pass  | **partially pass** |
        +-------------+------------------+---------------+--------------+-----------+-------+--------------------+

    \

    spyglass check of enc_rmd_top:
    2 "Av_range01" warnings are reported, but it's okay, because if cfg_num_mod_i is configured correctly, cnt_mod_d1_r and cnt_mod_d2_r will not be larger than 12.

    ::

        Array bound violation observed for cnt_mod_d1_r = 13 for dimension 1 of variable dat_buf_r where allowed range is [12:0] (Hier:enc_rmd_top.enc_rmd_cst.encRmdCstCore[0].core).
        Array bound violation observed for cnt_mod_d2_r = 13 for dimension 1 of variable dat_buf_r where allowed range is [12:0] (Hier:enc_rmd_top.enc_rmd_cst.encRmdCstCore[0].core).

    \

    .. table:: **simulation**
        :align: left
        :widths: auto

        +-------------+------------------+--------------------------------+---------------+
        | Module      | Version          | NCverilog                      | Vivado        |
        +=============+==================+================+===============+===============+
        | \                              | single         | regression    | single        |
        |                                +------+---------+-----+---------+-----+---------+
        |                                | rtl  | netlist | rtl | netlist | rtl | netlist |
        +-------------+------------------+------+---------+-----+---------+-----+---------+
        | enc_rmd_top | syn/20200914 + 3 | pass | \-      | \-  | \-      | pass| pass    |
        +-------------+------------------+------+---------+-----+---------+-----+---------+

    \

    .. table:: **synthesis**
        :align: left
        :widths: auto

        +-------------+------------------+---------+-------------------------+--------------+---------------------------------------------------------------------------------------------------+
        | Module      | Version          | Quartus | Vivado @ 150M           | DC @ 100M    | DC @ 500M                                                                                         |
        +=============+==================+=========+=========+=======+=======+==============+========+==============+=========================================+========+==============+=========+
        | \                              | report  | report  | area  | slack | logic        | report | logic        | memory                                  | slack  | clock gating | power   |
        |                                |         |         | (LUT) | (ns)  | (um^2)       |        | (um^2)       | (bit)                                   | (ns)   | (%)          | (mW)    |
        +-------------+------------------+---------+---------+-------+-------+--------------+--------+--------------+-----------------------------------------+--------+--------------+---------+
        | enc_rmd_top | syn/20200914 + 3 | pass    | pass    | 31972 | 1.176 | 76105.691178 | pass   | 86436.674022 | NUMB_BNK x SIZE_FRA_X/4 x DATA_PXL_WDx4 | 0.00   | 99.07        | 40.0622 |
        +-------------+------------------+---------+---------+-------+-------+--------------+--------+--------------+-----------------------------------------+--------+--------------+---------+
