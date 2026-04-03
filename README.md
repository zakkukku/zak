 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
new file mode 100644
index 0000000000000000000000000000000000000000..f3ebb0063eb2490c923dcf6cbacdae6eeca4d4eb
--- /dev/null
+++ b/README.md
@@ -0,0 +1,45 @@
+# Airdrop Assistant CLI (Python)
+
+Program command-line untuk bantu workflow airdrop:
+- Tambah campaign
+- Checklist task
+- Lihat progress
+- Pantau deadline
+
+> Gunakan hanya untuk aktivitas yang sesuai aturan platform/project.
+
+## Menjalankan
+
+```bash
+python3 airdrop_assistant.py --help
+```
+
+## Contoh penggunaan
+
+### 1) Tambah campaign
+
+```bash
+python3 airdrop_assistant.py add \
+  --name "LayerX" \
+  --platform "Galxe" \
+  --deadline "2026-04-30T23:59:00+00:00" \
+  --tasks "Follow X" "Join Discord" "Bridge tx"
+```
+
+### 2) Lihat progress
+
+```bash
+python3 airdrop_assistant.py list
+```
+
+### 3) Tandai task selesai
+
+```bash
+python3 airdrop_assistant.py done --campaign "LayerX" --task "Join Discord"
+```
+
+### 4) Cek deadline 48 jam ke depan
+
+```bash
+python3 airdrop_assistant.py remind --hours 48
+```
 
EOF
)
