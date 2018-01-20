# How I did it
1. Install `>= ansible2.4`
2. Create .vault_pass with password for decrypt(hint: Cheez knows it)
3. run
      ansible-playbook -i prod site.yml --vault-password-file .vault_pass
