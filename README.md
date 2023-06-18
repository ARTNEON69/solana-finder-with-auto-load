# solana-finder-with-auto-load
# Запуск через Докер для Майнета прямо из папки Solana

# сначала очистка докера:

sudo docker system prune -a
# после:
docker pull c29r3/solana-snapshot-finder:latest; \
sudo docker run -it --rm \
-v ~/solana/ledger:/solana/snapshot \
--user $(id -u):$(id -g) \
c29r3/solana-snapshot-finder:latest \
--snapshot_path /solana/snapshot
