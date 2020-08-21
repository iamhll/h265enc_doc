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
