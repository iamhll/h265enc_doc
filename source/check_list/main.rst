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

    \

(20201015) SRC and SIM Status
-----------------------------

    .. table:: **SRC**
        :align: left
        :widths: auto

        +-------------+------------------+------------------+--------------+
        | Module      | Hardware Version | Software Version | Status       |
        +=============+==================+==================+==============+
        | enc_rmd_top | syn/20201015     | syn/20200918     | Synchronized |
        +-------------+------------------+------------------+--------------+
        | enc_ime_top | syn/20201015     | syn/20200918     | Synchronized |
        +-------------+------------------+------------------+--------------+
        | enc_fme_top | syn/20201015     | syn/20200918     | Synchronized |
        +-------------+------------------+------------------+--------------+
        | enc_rdo_top | syn/20201015     | syn/20200918     | Synchronized |
        +-------------+------------------+------------------+--------------+

    \

    .. table:: **SIM**
        :align: left
        :widths: auto

        +-------------+--------------+-----------------------+----------------------+-----------------+
        | Module      | Version      | Check Point           | Checker              | Status          |
        +=============+==============+=======================+======================+=================+
        | enc_rmd_top | syn/20201015 | ram_mod_wr            | CHKO_RMD_TOP_MOD     | Synchronized    |
        +-------------+--------------+-----------------------+----------------------+-----------------+
        | enc_ime_top | syn/20201015 | fdb_flg_iip           | CHKO_IME_TOP_FLG_IIP | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_dat_prt           | CHKO_IME_TOP_PRT     | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_dat_qp            | CHKO_IME_TOP_QP      | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_dat_sam           | **None**             | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_dat_mad           | **None**             | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | ram_imv_wr            | CHKO_IME_TOP_IMV     | Synchronized    |
        +-------------+--------------+-----------------------+----------------------+-----------------+
        | enc_fme_top | syn/20201015 | ram_fmv_out_wr        | CHKO_FME_TOP_FMV     | Synchronized    |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | ram_pre_lu_wr         | CHKO_FME_TOP_PRE_LU  | Synchronized    |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | ram_pre_ch_wr         | CHKO_FME_TOP_PRE_CH  | Synchronized    |
        +-------------+--------------+-----------------------+----------------------+-----------------+
        | enc_rdo_top | syn/20201015 | fdb_flg_iip           | **None**             | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_enm_prt_cu,pu     | CHKO_RDO_TOP_PRT     | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_dat_cbf_cu_y,u,v  | **None**             | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | fdb_dat_cbf_4x4_y,u,v | **None**             | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | ram_mod_fnl_if        | CHKO_RDO_TOP_MOD     | **Out of Sync** |
        |             |              +-----------------------+----------------------+-----------------+
        |             |              | ram_rec_wr            | CHKO_RDO_TOP_REC     | Synchronized    |
        +-------------+--------------+-----------------------+----------------------+-----------------+

    \


(20201015) CHK, SIM and SYN Status
----------------------------------

    .. table:: **CHK**
        :align: left
        :widths: auto

        +-------------+--------------+---------------+--------------+-----------+-------+--------------------+-----------+
        | Module      | Version      | update script | check script | NCverilog | Verdi | Spyglass           | Formality |
        +=============+==============+===============+==============+===========+=======+====================+===========+
        | enc_rmd_top | syn/20201015 | pass          | pass         | pass      | pass  | **partially pass** | **TBT**   |
        +-------------+--------------+---------------+--------------+-----------+-------+--------------------+-----------+
        | enc_ime_top | syn/20201015 | pass          | pass         | pass      | pass  | **partially pass** | **TBT**   |
        +-------------+--------------+---------------+--------------+-----------+-------+--------------------+-----------+
        | enc_fme_top | syn/20201015 | pass          | pass         | pass      | pass  | **partially pass** | **TBT**   |
        +-------------+--------------+---------------+--------------+-----------+-------+--------------------+-----------+
        | enc_rdo_top | syn/20201015 | pass          | pass         | pass      | pass  | **partially pass** | **TBT**   |
        +-------------+--------------+---------------+--------------+-----------+-------+--------------------+-----------+

    \

    .. table:: **SIM**
        :align: left
        :widths: auto

        +-------------+--------------+--------------------------------+---------------+
        | Module      | Version      | NCverilog                      | Vivado        |
        +=============+==============+================+===============+===============+
        | \                          | single         | regression    | single        |
        |                            +------+---------+-----+---------+-----+---------+
        |                            | rtl  | netlist | rtl | netlist | rtl | netlist |
        +-------------+--------------+------+---------+-----+---------+-----+---------+
        | enc_rmd_top | syn/20201015 | pass | \-      | \-  | \-      | pass| pass    |
        +-------------+--------------+------+---------+-----+---------+-----+---------+
        | enc_ime_top | syn/20201015 | pass | \-      | \-  | \-      | pass| pass    |
        +-------------+--------------+------+---------+-----+---------+-----+---------+
        | enc_fme_top | syn/20201015 | pass | \-      | \-  | \-      | pass| pass    |
        +-------------+--------------+------+---------+-----+---------+-----+---------+
        | enc_rdo_top | syn/20201015 | pass | \-      | \-  | \-      | pass| pass    |
        +-------------+--------------+------+---------+-----+---------+-----+---------+

    \

    .. table:: **SYN**
        :align: left
        :widths: auto

        +-------------+--------------+---------+--------------------------+-------------------+------------------------------------------------------------------------------+
        | Module      | Version      | Quartus | Vivado @ 150M            | DC @100M @GF28SLP | DC @500M @GF28SLP                                                            |
        +=============+==============+=========+=========+=======+========+===================+========+===================+===============+=======+==============+==========+
        | \                          | report  | report  | area  | slack  | logic             | report | logic             | memory        | slack | clock gating | power    |
        |                            |         |         | (LUT) | (ns)   | (um^2)            |        | (um^2)            | (um^2)        | (ns)  | (%)          | (mW)     |
        +-------------+--------------+---------+---------+-------+--------+-------------------+--------+-------------------+---------------+-------+--------------+----------+
        | enc_rmd_top | syn/20201015 | pass    | pass    | 31972 |  1.176 | 076105.691178     | pass   | 086436.674022     | 015702.413086 | 0.00  | 99.07        | 40.0622  |
        +-------------+--------------+---------+---------+-------+--------+-------------------+--------+-------------------+---------------+-------+--------------+----------+
        | enc_ime_top | syn/20201015 | pass    | pass    | 38418 |  1.270 | **181110.848368** | pass   | **188418.317291** | 063462.755859 | 0.00  | 99.55        | 197.0432 |
        +-------------+--------------+---------+---------+-------+--------+-------------------+--------+-------------------+---------------+-------+--------------+----------+
        | enc_fme_top | syn/20201015 | pass    | pass    | 39122 | -2.683 | **144087.721395** | pass   | **192376.897133** | 007851.206543 | 0.00  | 98.28        | 24.5931  |
        +-------------+--------------+---------+---------+-------+--------+-------------------+--------+-------------------+---------------+-------+--------------+----------+
        | enc_rdo_top | syn/20201015 | pass    | pass    | 71122 | -0.420 | **548707.646507** | pass   | **678454.444482** | 152797.522949 | 0.00  | **96.61**    | 24.3888  |
        +-------------+--------------+---------+---------+-------+--------+-------------------+--------+-------------------+---------------+-------+--------------+----------+

    spyglass check of enc_rmd_top (syn/20201015):

    *   2 "Av_range01" warnings are reported

        ::

            Av_range01 @ ../../src/enc/enc_knl/enc_rmd/enc_rmd_cst_knl.v:319
            description: Array bound violation observed for cnt_mod_d1_r = 13 for dimension 1 of variable dat_buf_r where allowed range is [12:0] (Hier:enc_rmd_top.enc_rmd_cst.\encRmdCstKnl[0].knl ).
            code       :   assign dat_pre_d1_w = dat_buf_r[cnt_mod_d1_r] ;

            Av_range01 @ ../../src/enc/enc_knl/enc_rmd/enc_rmd_cst_knl.v:365
            description: Array bound violation observed for cnt_mod_d2_r = 13 for dimension 1 of variable dat_buf_r where allowed range is [12:0] (Hier:enc_rmd_top.enc_rmd_cst.\encRmdCstKnl[0].knl ).
            code       :   assign dat_o = dat_buf_r[cnt_mod_d2_r] ;

    spyglass check of enc_ime_top (syn/20201015):

    *   3 "Av_deadcode01" warnings are reported

        ::

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_ime/enc_ime_ref_ver.v:473
            description: Dead code exists as condition is always false[hier: enc_ime_ref_ver_get_ref]
            code       :         7'd64 : ref_o = ref_i >> (`IME_DATA_PXL_WD*(NUMB_PXL_INP-NUMB_PXL_OUT-'d64)) ;

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_ime/enc_ime_adr.v:682
            description: Dead code exists as condition is always false[hier: enc_ime_adr_cst_imv]
            code       :         8'b1???_???? :    bit_imv_x_w = 'd21 ;

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_ime/enc_ime_adr.v:697
            description: Dead code exists as condition is always false[hier: enc_ime_adr_cst_imv]
            code       :         7'b1??_???? :    bit_imv_y_w = 'd19 ;

    spyglass check of enc_fme_top (syn/20201015):

    *   2 "Av_range01" warnings are reported

        ::

            Av_range01 @ ../../src/common/sram_tp_reg_based.v:72
            description: Array bound violation observed for \ramEncRdoRecTsps[0].buf_wr_adr_r  = 0 for dimension 1 of variable mem_array (Hier:enc_fme_top.enc_fme_pre_lu.enc_fme_tsps_even.\ramEncRdoRecTsps[0].ram_enc_fme_tsps ).
            code       :       mem_array[wr_adr_i] <= wr_dat_i ;

            Av_range01 @ ../../src/common/sram_tp_reg_based.v:92
            description: Array bound violation observed for \ramEncRdoRecTsps[0].buf_rd_adr_r  = 0 for dimension 1 of variable mem_array (Hier:enc_fme_top.enc_fme_pre_ch.enc_fme_tsps_even.\ramEncRdoRecTsps[0].ram_enc_fme_tsps ).
            code       :       rd_dat_r <= mem_array[rd_adr_i] ;

    \

    spyglass check of enc_rdo_top (syn/20201015):

    *   4 "Av_range01" warnings are reported

        ::

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_rdo/enc_rdo_trv/enc_rdo_trv_mpm.v:273
            description: Dead code exists as condition is always false[hier: enc_rdo_trv_mpm]
            code       :         else if( ini_val_r ) begin

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_rdo/enc_rdo_top.v:1057
            description: Dead code exists as condition is always false (reason: static nets in fanin cone) [hier: enc_rdo_top]
            code       :       DATA_SYN_TRV : begin

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_rdo/enc_rdo_top.v:2021
            description: Dead code exists as condition is always false (reason: static nets in fanin cone) [hier: enc_rdo_top]
            code       :         DATA_SYN_TRV :    DEC_ena_w = 'd0 ;

            Av_deadcode01 @ ../../src/enc/enc_knl/enc_rdo/enc_rdo_top.v:2326
            description: Dead code exists as condition is always false (reason: static nets in fanin cone) [hier: enc_rdo_top]
            code       :         DATA_SYN_TRV : begin    ram_mod_fnl_enm_chn_o       = TRV_ram_mod_wr_enm_chn_o_w       ;
