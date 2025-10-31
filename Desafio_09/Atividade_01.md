CREATE OR REPLACE TRIGGER trg_log_insert_vendas

AFTER UPDATE ON VENDAS

F0R EACH ROW

BEGIN
	INSERT INTO LOG_VENDAS (
	    operacao,
        id_venda,
        produto,
        vendedor,
        valor,
        usuario,
        data_hora,
        observacao
	)	VALUES (
		'INSERT',
		:NEW.id,
        :NEW.produto,
        :NEW.vendedor,
        :NEW.valor,
		USER,
		SYSDATE,
		'Nova venda inserida: ' || :New.produto || ' vendido por ' || :NEW.vendedor);
		END;
		/
