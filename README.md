# nexuslabandroid
How to run the NexusLab Prover on Your Android device

# 1. Update Termux and Install Dependencies

pkg update -y
pkg upgrade -y
pkg install git curl protobuf rust openssl -y
termux-setup-storage

# 2. Set Environment Variables for OpenSSL

export OPENSSL_DIR=/data/data/com.termux/files/usr
export OPENSSL_INCLUDE_DIR=/data/data/com.termux/files/usr/include
export OPENSSL_LIB_DIR=/data/data/com.termux/files/usr/lib
export PKG_CONFIG_ALLOW_SYSTEM_CFLAGS=1
export PKG_CONFIG_PATH=/data/data/com.termux/files/usr/lib/pkgconfig

# 3. Ensure You Are in the Correct Directory The cargo build command should be run inside a valid Rust project directory. If you don’t already have a project, create one:

cargo new my_project
cd my_project

# 4. Run cargo build Inside the project directory, run:

cargo build

# 5. Install Nexus CLI After successfully building your Rust project, run the curl command:

curl -s https://cli.nexus.xyz | sh

# This command downloads and runs the Nexus CLI installation script. Please make sure you have enough permissions and an internet connection.

# Notes
# If Nexus CLI requires a specific setup:
# Some tools or scripts (like curl cli.nexus.xyz | sh) might assume certain prerequisites. Verify the Nexus CLI documentation for any specific setup instructions.
# Verify Rust Installation:
# Ensure Rust and Cargo are installed correctly:

rustc --version
cargo --version

# If you still face issues, provide the exact error message for further troubleshooting

