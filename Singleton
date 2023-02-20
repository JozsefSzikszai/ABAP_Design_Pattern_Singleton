CLASS lcl_class DEFINITION CREATE PRIVATE.

  PUBLIC SECTION.
    CLASS-METHODS: get_instance IMPORTING iv_number       TYPE i
                                RETURNING VALUE(ro_class) TYPE REF TO lcl_class.

  PRIVATE SECTION.
    CLASS-DATA: mo_singleton TYPE REF TO lcl_class.
    DATA: mv_number.
    METHODS: constructor IMPORTING iv_number TYPE i.

ENDCLASS.

CLASS lcl_class IMPLEMENTATION.

  METHOD get_instance.

    IF mo_singleton IS INITIAL.
      mo_singleton = NEW #( iv_number ).
    ENDIF.
    ro_class = mo_singleton.

  ENDMETHOD.

  METHOD constructor.

    mv_number = iv_number.

  ENDMETHOD.

ENDCLASS.
