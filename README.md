# Python_Os_modulu en çok kulanım komutları ve sırayla örnekleri.

import os

# 1. Çalışma Dizini İşlemleri
current_directory = os.getcwd()
print("Mevcut Çalışma Dizini:", current_directory)

# 2. Dizin İşlemleri
workspace_name = "my_workspace"
workspace_path = os.path.join(current_directory, workspace_name)

# Dizin oluşturma
os.mkdir(workspace_path)
print(f"{workspace_name} dizini oluşturuldu.")

# Alt dizin oluşturma
subdirectory_path = os.path.join(workspace_path, "subdirectory")
os.makedirs(subdirectory_path)
print("Alt dizin oluşturuldu.")

# 3. Dizin ve Dosya Varlık Kontrolü
if os.path.exists(subdirectory_path):
    print(f"{subdirectory_path} dizini var.")

# 4. Dizin ve Dosya Silme
os.rmdir(subdirectory_path)
print("Alt dizin silindi.")

# 5. Yol İşlemleri
file_path = os.path.join(workspace_path, "example.txt")
print("Dosya Yolu:", file_path)

# 6. Çevre Değişkenleri
environment_variables = os.environ
print("Çevre Değişkenleri:", environment_variables)

# 7. İşletim Sistemi Bağımsızlığı
os_type = os.name
print("İşletim Sistemi Türü:", os_type)

# 8. Dosya ve Dizin Adları İşlemleri
file_name = os.path.basename(file_path)
directory_name = os.path.dirname(file_path)
print("Dosya Adı:", file_name)
print("Dizin Adı:", directory_name)



"""
Bu örnekte, os modülü kullanılarak bir çalışma alanı oluşturulur, bu alan içinde bir alt dizin ve bir dosya eklenir, ardından bu dosya ve dizinlerin varlık kontrolü yapılır, silinir, yollar birleştirilir ve ayrılır, çevre değişkenleri ve işletim sistemi türü elde edilir.
"""
