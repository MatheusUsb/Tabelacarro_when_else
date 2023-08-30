# Tabelacarro_when_else

CREATE TABLE TabelaCarros (
    carro VARCHAR(50),
    marca VARCHAR(50),
    valor DECIMAL(10, 2),
    popularidade VARCHAR(20)
);

INSERT INTO TabelaCarros (carro, marca, valor)
VALUES
    ('Fiesta', 'Ford', 15000.00),
    ('Gol', 'Volkswagen', 18000.00),
    ('Civic', 'Honda', 25000.00),
    ('Onix', 'Chevrolet', 22000.00),
    ('Uno', 'Fiat', 15000.00),
    ('Corolla', 'Toyota', 28000.00),
    ('Palio', 'Fiat', 17000.00),
    ('Sandero', 'Renault', 19000.00),
    ('Ka', 'Ford', 16000.00),
    ('HB20', 'Hyundai', 21000.00);

UPDATE TabelaCarros
SET popularidade = CASE
    WHEN valor <= 20000.00 THEN 'Popular'
    ELSE 'Não Popular'
END;

SELECT * FROM TabelaCarros;
