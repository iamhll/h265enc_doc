.. -----------------------------------------------------------------------------
    ..
    ..  Filename       : main.rst
    ..  Author         : Huang Leilei
    ..  Created        : 2020-07-12
    ..  Description    : coding style related documents
    ..
.. -----------------------------------------------------------------------------

Coding Style
============

(20200921) Basic Rules
----------------------


#.  Indentation

    use 2 spaces

    \

#.  Combinational block

    ::

        reg [4-1 :0]    condition_r ;

        always @(*) begin
                       dat_w = 'd7 ;
          case( condition_r )
            4'd00 :    dat_w = 'd3 ;
            4'd07 :    dat_w = 'd2 ;
            4'd09 :    dat_w = 'd5 ;
            4'd20 :    dat_w = 'd9 ;
          encase
        end

#.  Sequential block

    ::

        reg [4-1 :0]    condition_r ;

        always @(posedge clk or negedge rstn ) begin
          if( !rstn ) begin
            dat_r <= 'd0 ;
          end
          else begin
                         dat_r <= 'd0 ;
            case( condition_r )
              4'd00 :    dat_r <= 'd3 ;
              4'd07 :    dat_r <= 'd2 ;
              4'd09 :    dat_r <= 'd5 ;
              4'd20 :    dat_r <= 'd9 ;
            encase
          end
        end

#.  Placing begin and end

    always use begin and end

    ::

        always @(*) begin
          if( condition ) begin
            one statement ;
          end
          else begin
            one statement ;
          end
        end

#.  Spaces

    ::

        always(*)
        always(posedge clk or negdege rstn ) begin
        if( condition )
        assign dat_w = dat_0_w * dat_1_w ;
        assign dat_w = (dat_0_w+dat_1_w) * dat_2_w ;

#.  Naming

    use small cases, digits and "_" for variables

    ::

        dat_pre_w
        dat_coe_r

    use big cases, digits and "_" for parameters and definitions

    ::

        DATA_INP_WD
        `DATA_PXL_WD

    use the following prefix or postfix to indicate variable types

    ::

        _i, input
        _o, output

        _w, combinational logic
        _d?_w, combinational logic in stage ?
        _r, sequential logic
        _d?_r, sequential logic in stage ?

        val_, valid
        flg_, flag
        num_, number
        cnt_, counter
        idx_, index
        enm_, enumerator
        dat_, data

        gvIdx, index in generation block 
        lpIdx, index in for loop

#.  Digits

    always put type before digits (except those in width declaration)

    ::

        'd63
        'sd63
        'h3f
        'sh3f
