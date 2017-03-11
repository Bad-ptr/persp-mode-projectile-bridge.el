# persp-mode-projectile-bridge  

persp-mode projectile integration  

## Installation  

`M-x package-install-file RET persp-mode-projectile-bridge.el RET`

## How to configure  

```elisp

    (with-eval-after-load "persp-mode-projectile-bridge-autoloads"
      (add-hook 'persp-mode-projectile-bridge-mode-hook
                #'(lambda ()
                    (if persp-mode-projectile-bridge-mode
                        (persp-mode-projectile-bridge-find-perspectives-for-all-buffers)
                      (persp-mode-projectile-bridge-kill-perspectives))))
      (add-hook 'after-init-hook
                #'(lambda ()
                    (persp-mode-projectile-bridge-mode 1))
                t))

```
