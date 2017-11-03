# CIDR-Calculator

Tugas Kecil IF3130 Jaringan Komputer

__Prerequisites__
This assignment is run by:
1. Makefile
2. Python 2.7

__How To Run__
1. Type 'make run' on your terminal in Linux!

__Explanation of Each Phase Process__

__Phase 1__

Pada phase ini yang dijalankan adalah fungsi getValidSubnet().
Untuk mencari subnet yang cocok dengan host yang dapat dilakukan adalah  menambahkan "+ /32" di setiap host.
Hal ini karena subnet dengan "ip address + /32" valid untuk host "ip address" untuk semua ip address.


__Phase 2__

Pada phase ini yang dijalankan adalah fungsi countHosts().
Kita berusaha mendapatkan nilai dari subnet mask (yaitu angka yang berada di belakang "/").
Banyaknya host adalah 2**(32-nilai subnet mask).

__Phase 3__

Pada phase ini yang dijalankan adalah fungsi isSubnetValid().
Sebelumnya dibuat dulu fungsi ipToInt(). Fungsi ini berfungsi mengubah sebuah ip address dengan format x.x.x.x menjadi bentuk integernya.
Parameter masukan dari fungsi isSubnetValid() adalah subnet dan host. int_host adalah bentuk integer dari host. Untuk subnet akan dilakukan
split berdasarkan tanda "/", string sebelum "/" disimpan dalam subnet_ip, sedangkan string setelah "/" disimpan dalam subnet_mask.
int_subnet_ip menyimpan bentuk integer dari subnet_ip. Sedangkan int_subnet_mask menyimpan bentuk integer dari subnet_mask.
mask memiliki nilai 0xffffffff di shift left sebanyak (32-int_subnet_mask) dan dilakukan operasi binary AND dengan 0xffffffff.
Apabila nilai operasi binary AND dari int_host dan mask sama dengan nilai operasi binary AND dari int_subnet_ip dan mask, maka akan menghasilkan "T", yaitu host berada di dalam subnet tersebut. Dan "F" untuk sebaliknya


# Authors
Patrick Nugroho Hadiwinoto (NIM 13515040)