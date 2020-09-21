.. -----------------------------------------------------------------------------
    ..
    ..  Filename       : main.rst
    ..  Author         : Huang Leilei
    ..  Created        : 2020-07-12
    ..  Description    : template related documents
    ..
.. -----------------------------------------------------------------------------

Template
========

    |   For a detailed template, please refer to /src/enc/enc_knl/enc_rmd and /sim/rtl_enc_rmd_top.
    |   For a rough template, please check the following contents.


(20200921) Design
-----------------

::

    //------------------------------------------------------------------------------
      //
      //  The confidential and proprietary information contained in this file may
      //  only be used by a person authorised under and to the extent permitted
      //  by a subsisting licensing agreement from XK Silicon.
      //
      //                   (C) COPYRIGHT 2020 XK Silicon.
      //                       ALL RIGHTS RESERVED
      //
      //  This entire notice must be reproduced on all copies of this file
      //  and copies of this file may only be made by a person if such person is
      //  permitted to do so under the terms of a subsisting license agreement
      //  from XK Silicon.
      //
      //  Revision       : 112933
      //  Release        : XK265
      //
    //------------------------------------------------------------------------------
      //
      //  Filename       : ???.v
      //  Author         : ???
      //  Created        : ???-??-??
      //  Description    : [logic] to [???] or [wrapper] for [???] or [top] of [???]
      //
    //------------------------------------------------------------------------------
      //
      //  Modified       : ???-??-?? by ???
      //  Description    : ???
      //
    //------------------------------------------------------------------------------

    `include "defines_enc.vh"

    module ???(
      // global
      clk                 ,
      rstn                ,
      // cfg_i
      cfg_???_i           ,
      // ctl_if
      start_i             ,
      done_o              ,
      // dat_i
      val_i               ,
      dat_i               ,
      // dat_o
      val_o               ,
      dat_o               ,
      // fdb_o
      fdb_???_o           ,
      // ram_???_rd
      ram_???_rd_val_o    ,
      ram_???_rd_adr_o    ,
      ram_???_rd_val_i    ,
      ram_???_rd_dat_o    ,
      // ram_???_wr
      ram_mod_wr_val_o    ,
      ram_mod_wr_adr_o    ,
      ram_mod_wr_dat_o    ,
      // ram_???_if
      ram_???_adr_o       ,
      ram_???_rd_val_o    ,
      ram_???_rd_val_i    ,
      ram_???_rd_dat_i    ,
      ram_???_wr_val_o    ,
      ram_???_wr_dat_o
    );


    //*** PARAMETER ****************************************************************

      // global
      parameter    ???     = -1             ;    // ??? -> ???

      // local
      localparam   ???     = ???            ;    // ??? -> ???

      // derived
      localparam   ???     = ???            ;    // ??? -> ???


    //*** INPUT/OUTPUT *************************************************************

      // global
      input                clk              ;
      input                rstn             ;

      // cfg_i
      input  [???-1 :0]    cfg_???_i        ;    // cfg -> configuration; ??? -> ???

      // ctl_if
      input                start_i          ;
      output               done_o           ;

      // dat_i
      input                val_i            ;    // val -> valid
      input  [???-1 :0]    dat_i            ;    // dat -> data

      // dat_i
      output               val_o            ;    // val -> valid
      output [???-1 :0]    dat_o            ;    // dat -> data

      // fdb_i
      output [???-1 :0]    fdb_???_o        ;    // fdb -> feedback; ??? -> ???

      // ram_???_rd
      output               ram_???_rd_val_o ;    // ??? -> ???; rd -> read; val -> valid
      output [???-1 :0]    ram_???_rd_adr_o ;    // adr -> address
      input                ram_???_rd_val_i ;
      input  [???-1 :0]    ram_???_rd_dat_i ;    // dat -> data

      // ram_???_wr
      output               ram_???_wr_val_o ;    // ??? -> ???; wr -> write; val -> valid
      output [???-1 :0]    ram_???_wr_adr_o ;    // adr -> address
      output [???-1 :0]    ram_???_wr_dat_o ;    // dat -> data

      // ram_???_if
      output [???-1 :0]    ram_???_adr_o    ;    // ??? -> ???; adr -> address
      output               ram_???_rd_val_o ;    // rd -> read
      input                ram_???_rd_val_i ;
      input  [???-1 :0]    ram_???_rd_dat_i ;    // dat -> data
      output               ram_???_wr_val_o ;    // wr -> write
      output [???-1 :0]    ram_???_wr_dat_o ;


    //*** WIRE/REG *****************************************************************

      // global

      // stage 0

      // stage 1

      // stage n

      // output


    //*** MAIN BODY ****************************************************************
    //--- GLOBAL ---------------------------
      assign { dat_0_i
              ,dat_1_i
              ,dat_2_i
              ,dat_3_i
      } = dat_i ;


    //--- STAGE 0 --------------------------
      // ???
      always @(*) begin
                   ??? = ??? ;
        case( ??? )
          ??? :    ??? = ??? ;
          ??? :    ??? = ??? ;
          ??? :    ??? = ??? ;
          ??? :    ??? = ??? ;
        endcase
      end

      // ???
      always @(posedge clk or negedge rstn ) begin
        if( !rstn ) begin
          ??? <= 'd0 ;
        end
        else begin
          if( val_i ) begin
            ??? <= ??? ;
          end
        end
      end


    //--- STAGE 1 --------------------------
      ???


    //--- STAGE n --------------------------
      ???


    //--- OUTPUT ---------------------------
      ???


    //*** DEBUG ********************************************************************

      `ifdef DBUG_ENC

        // sanity check
        ???

        // synchronization check
        ???

        // observation point
        ???

      `endif

    endmodule


    //*** SUBMODULE ****************************************************************
    //--- ??? ------------------------------
      module ???(
        clk      ,
        rstn     ,
        val_i    ,
        dat_i    ,
        val_o    ,
        dat_o
        );

        // paramter
        parameter    ??? = -1  ;

        localparam   ??? = ??? ;

        localparam   ??? = ??? ;

        // input/output
        input                    clk   ;
        input                    rstn  ;

        input                    val_i ;
        input      [???-1 :0]    dat_i ;

        output reg               val_o ;
        output     [???-1 :0]    dat_o ;

        // wire/reg
        ???

        // main body
        ???

      endmodule

    `include "undefines_enc.vh"


(20200921) Testbench
--------------------

::

    //------------------------------------------------------------------------------
      //
      //  Filename       : sim_???.v
      //  Author         : ???
      //  Created        : ????-??-??
      //  Description    : [testbench] for [???]
      //
    //------------------------------------------------------------------------------
      //
      //  Modified       : ????-??-?? by ???
      //  Description    : ???
      //
    //------------------------------------------------------------------------------

    //--- GLOBAL ---------------------------
      // DUT
      //`define DUT_TOP                       -1
      //`define DUT_TOP_STR                   -1

      `include "check_data/dut_setting.vh"

      // SIM
      //`define SIM_TOP                       -1
      //`define SIM_TOP_STR                   -1

      //`define STP_LVL                       -1

      //`define DMP_SHM                       -1
        `define DMP_SHM_FILE                  "simul_data/wave_form.shm"
      //`define DMP_SHM_BGN                   -1
      //`define DMP_SHM_LVL                   -1

      //`define SEED                          -1
      //`define DBUG                          -1


    //--- LOCAL (VARIABLE) -----------------
      // SIM (chko)
      `define CHKO                            "on"
        `define CHKO_???                        "on"

        `ifdef DBUG
          `define CHKO_???                    `DBUG
          `define CHKO_???                    `DBUG
        `endif

      // SIM (dump)
      //`define DUMP_FSDB
        `define DUMP_FSDB_BGN                 0
      //`define DUMP_VCD
        `define DUMP_VCD_BGN                  0
      //`define DUMP_EVCD
        `define DUMP_EVCD_BGN                 0

      // DUT (implementation)
      //`define IMPL_BEHAVE
      //`define IMPL_FPGA

      // DUT (debug)
      `ifdef DBUG
        `define DBUG_ENC
      `endif

      // DUT (setting)

      // DUT (other)
      // !!! now defines_enc.vh must be put here
      `include "defines_enc.vh"


    //--- LOCAL (CONSTANT) -----------------
      // SIM (clk)
      `define CLK_FULL                        10
      `define CLK_HALF                        ( `CLK_FULL / 2 )

      // SIM (init)
      `define INIT_???_FILE                   "check_data/???.dat"

      // SIM (chko: normal)
      `define CHKO_???_FILE                   "check_data/???.dat"

      // SIM (chko: verbose)
      `define CHKO_???_FILE                   "check_data/???.dat"

      // SIM (dump)
      `define DUMP_FSDB_FILE                  "simul_data/wave_form.fsdb"
      `define DUMP_VCD_FILE                   "simul_data/wave_form.vcd"
      `define DUMP_EVCD_FILE                  "simul_data/wave_form.evcd"


    module `SIM_TOP ;

    //*** PARAMETER ****************************************************************

      `include "parameters_enc.vh"


    //*** INPUT/OUTPUT *************************************************************

      // global
      reg                clk              ;
      reg                rstn             ;

      // cfg_i
      reg  [???-1 :0]    cfg_???_i        ;

      // ctl_if
      reg                start_i          ;
      wire               done_o           ;

      // dat_i
      reg                val_i            ;
      reg  [???-1 :0]    dat_i            ;

      // dat_i
      wire               val_o            ;
      wire [???-1 :0]    dat_o            ;

      // fdb_i
      wire [???-1 :0]    fdb_???_o        ;

      // ram_???_rd
      wire               ram_???_rd_val_o ;
      wire [???-1 :0]    ram_???_rd_adr_o ;
      reg                ram_???_rd_val_i ;
      reg  [???-1 :0]    ram_???_rd_dat_i ;

      // ram_???_wr
      wire               ram_???_wr_val_o ;
      wire [???-1 :0]    ram_???_wr_adr_o ;
      wire [???-1 :0]    ram_???_wr_dat_o ;

      // ram_???_if
      wire [???-1 :0]    ram_???_adr_o    ;
      wire               ram_???_rd_val_o ;
      reg                ram_???_rd_val_i ;
      reg  [???-1 :0]    ram_???_rd_dat_i ;
      wire               ram_???_wr_val_o ;
      wire [???-1 :0]    ram_???_wr_dat_o ;


    //*** WIRE/REG *****************************************************************

      // seed
      integer            seed_r                 ;

      // counter
      integer            cnt_???_r              ;


    //*** SUB BENCH ****************************************************************

      `include "sub_bench/sub_bench.vh"


    //*** MAIN BODY ****************************************************************
    //--- PROC -----------------------------
      // clk
      initial begin
        clk = 'd0 ;
        forever begin
          #`CLK_HALF ;
          clk = ! clk ;
        end
      end

      // rstn
      initial begin
        rstn = 'd0 ;
        #( 5 * `CLK_FULL );
        @(negedge clk );
        rstn = 'd1 ;
      end

      // seed
      initial begin
        seed_r = `SEED ;
      end

      // main
      initial begin
        // init
        cfg_???_i = 'd0 ;
        start_i   = 'd0 ;
        val_i     = 'd0 ;
        dat_i     = 'd0 ;

        // delay
        #( 5 * `CLK_FULL );

        // log
        $display( "\n\n*** CHECK %s BEGIN ! ***\n" ,`DUT_TOP_STR );

        // delay
        #( 5 * `CLK_FULL );
        $display( "" );

        // core
        cnt_gop_r = 'd0 ;
        for( cnt_fra_r = 'd0 ;cnt_fra_r < `NUMB_FRA ;cnt_fra_r = cnt_fra_r + cnt_dlt_r ) begin
          if( cnt_gop_r == 'd0 ) begin
            for( cnt_lcu_y_r = 'd0 ;cnt_lcu_y_r < ((`SIZE_FRA_Y+`SIZE_LCU-'d1)/`SIZE_LCU) ;cnt_lcu_y_r = cnt_lcu_y_r + cnt_dlt_r ) begin
              for( cnt_lcu_x_r = 'd0 ;cnt_lcu_x_r < ((`SIZE_FRA_X+`SIZE_LCU-'d1)/`SIZE_LCU) ;cnt_lcu_x_r = cnt_lcu_x_r + cnt_dlt_r ) begin
                // init
                cfg_idx_bnk_i = $random(seed_r) % `NUMB_BNK ;
                cnt_dlt_r = cfg_idx_bnk_i == `INDX_BNK ;
                -> init_???_event ;

                // delay
                // !!! this delay is essential
                #( 5 * `CLK_FULL );

                // log
                $write( "\t at %08d ns, launching FRA %02d BNK %01d LCU %03d-%03d ... " ,$time ,cnt_fra_r ,cfg_idx_bnk_i ,cfg_pos_lcu_y_i ,cfg_pos_lcu_x_i );

                // start
                @(negedge clk );
                start_i = 'd1 ;
                @(posedge clk );
                cyc_bgn_r = $time / `CLK_FULL ;
                @(negedge clk );
                start_i = 'd0 ;

                // wait
                @(posedge done_o );
                @(posedge clk );
                cyc_end_r = $time / `CLK_FULL ;
                $display( "(delta cycle %04d)" ,(cyc_end_r-cyc_bgn_r) );

                // delay
                #( 10 * `CLK_FULL );
              end
            end
          end
          else begin
            // init
            cnt_dlt_r = 'd1 ;

            // log
            $display( "\t at %08d ns, skipping  FRA %02d BNK A LCU %03d-%03d..." ,$time ,cnt_fra_r ,cfg_pos_lcu_y_i ,cfg_pos_lcu_x_i );
          end

          // cnt_gop_r
          // !!! this delay is added to ensure that
          // !!! 1. every init or chki begins
          // !!! 2. every chko ends
          #( 10 * `CLK_FULL );
          cnt_gop_r = (cnt_gop_r+cnt_dlt_r) % `SIZE_GOP ;
          #( 10 * `CLK_FULL );
        end

        // log
        #( 1000 * `CLK_FULL );
        $display( "\n\n*** CHECK %s END ! ***\n" ,`DUT_TOP_STR );
        $finish;
      end


    //--- INST -----------------------------
      // begin of DUT
        `DUT_TOP dut(
          // global
          .clk                 ( clk                 ),
          .rstn                ( rstn                ),
          // cfg_i
          .cfg_???_i           ( cfg_???_i           ),
          // ctl_if
          .start_i             ( start_i             ),
          .done_o              ( done_o              ),
          // dat_i
          .val_i               ( val_i               ),
          .dat_i               ( dat_i               ),
          // dat_i
          .val_o               ( val_o               ),
          .dat_o               ( dat_o               ),
          // fdb_i
          .fdb_???_o           ( fdb_???_o           ),
          // ram_???_rd
          .ram_???_rd_val_o    ( ram_???_rd_val_o    ),
          .ram_???_rd_adr_o    ( ram_???_rd_adr_o    ),
          .ram_???_rd_val_i    ( ram_???_rd_val_i    ),
          .ram_???_rd_dat_i    ( ram_???_rd_dat_i    ),
          // ram_???_wr
          .ram_???_wr_val_o    ( ram_???_wr_val_o    ),
          .ram_???_wr_adr_o    ( ram_???_wr_adr_o    ),
          .ram_???_wr_dat_o    ( ram_???_wr_dat_o    ),
          // ram_???_if
          .ram_???_adr_o       ( ram_???_adr_o       ),
          .ram_???_rd_val_o    ( ram_???_rd_val_o    ),
          .ram_???_rd_val_i    ( ram_???_rd_val_i    ),
          .ram_???_rd_dat_i    ( ram_???_rd_dat_i    ),
          .ram_???_wr_val_o    ( ram_???_wr_val_o    ),
          .ram_???_wr_dat_o    ( ram_???_wr_dat_o    )
        );
      // end   of DUT

      // begin of SIM_???
      // end   of SIM_???


    //--- DUMP -----------------------------
      // shm
      `ifdef DMP_SHM
        initial begin
          if( `DMP_SHM=="on" ) begin
            #`DMP_SHM_BGN ;
            $shm_open( `DMP_SHM_FILE );
            $shm_probe( `SIM_TOP ,`DMP_SHM_LVL );
            #( 10 * `CLK_FULL );
            $display( "\t\t dump (shm,%s) to this test is on!" ,`DMP_SHM_LVL );
          end
        end
      `endif

      // fsdb
      `ifdef DUMP_FSDB
        initial begin
          #`DUMP_FSDB_BGN ;
          $fsdbDumpfile( `DUMP_FSDB_FILE );
          $fsdbDumpvars( `SIM_TOP );
          #( 10 * `CLK_FULL );
          $display( "\t\t dump (fsdb) to this test is on!" );
        end
      `endif

      // vcd
      `ifdef DUMP_VCD
        initial begin
          #`DUMP_VCD_BGN ;
          $dumpfile( `DUMP_VCD_FILE );
          $dumpvars( 'd0, `SIM_TOP );
          #( 10 * `CLK_FULL );
          $display( "\t\t dump (vcd) to this test is on!" );
        end
      `endif

      // evcd
      `ifdef DUMP_EVCD
        initial begin
          #`DUMP_EVCD_BGN ;
          $dumpports( dut ,`DUMP_EVCD_FILE );
          #( 10 * `CLK_FULL );
          $display( "\t\t dump (evcd) to this test is on!" );
        end
      `endif


    //*** DEBUG ********************************************************************

      `ifdef DBUG_ENC

      `endif

    endmodule

    `include "undefines_enc.vh"


(20200921) Subbench
--------------------

::

    //------------------------------------------------------------------------------
      //
      //  Filename       : sub_bench_???.vh
      //  Author         : ???
      //  Created        : ????-??-??
      //  Description    : [sub-testbench: ???] for [???]
      //
    //------------------------------------------------------------------------------
      //
      //  Modified       : ????-??-?? by ???
      //  Description    : ???
      //
    //------------------------------------------------------------------------------

    //--- CHKO_??? -----------------
    `ifdef ???
      initial begin
        ??? ;
      end

      task ??? ;
        // variables
        integer                sim_??? ;
        reg     [??? -1 :0]    sim_??? ;

        integer                dut_??? ;
        reg     [??? -1 :0]    dut_??? ;

        // main body
        begin
          if( (`CHKO=="on") && (`CHKO_???=="on") ) begin
            // log info
            #( 10 * `CLK_FULL );
            $display( "\t\t function check to ???'s ??? is on!" );

            // open files
            sim_fpt = $fopen( `CHKO_???_FILE ,"r" );

            // core loop
            forever begin
              // wait
              @(negedge clk );

              // dut_val
              dut_val = `PATH_RMD_TOP.??? ;

              // if valid
              if( dut_val ) begin
                // dut_*
                dut_??? = `PATH_RMD_TOP.??? ;

                // sim_*
                sim_fpt = ??? ;

                // dut_skp
                dut_skp = ???

                // check
                if( !dut_skp && (dut_dat!==sim_dat) ) begin
                  $display("\n\t ??? ERROR: at %08d ns, ??? (FRA %02d LCU %02d-%02d B4X4 %02d-%02d SIZ %02d ???) should be %x, however is %x!\n"
                    ,$time
                    ,cnt_fra_r
                    ,dut_pos_lcu_y
                    ,dut_pos_lcu_x
                    ,dut_pos_4x4_y
                    ,dut_pos_4x4_x
                    ,dut_dat_siz
                    ,???
                    ,sim_dat
                    ,dut_dat
                  );
                  if( `STP_LVL != "none" ) begin
                    #( 1000 * `CLK_FULL );
                    $finish ;
                  end
                end
              end
            end
          end
        end
      endtask
    `endif
