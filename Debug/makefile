################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/wav/subdir.mk
-include src/fatfs/subdir.mk
-include src/UART/subdir.mk
-include src/Timer16_32/subdir.mk
-include src/SPI/subdir.mk
-include src/PWM/subdir.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: WAVPlayer.axf

# Tool invocations
WAVPlayer.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"/home/evaota/LPCXpresso/workspace/CMSISv1p30_LPC11xx/Debug" -Xlinker -Map="WAVPlayer.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m0 -mthumb -T "WAVPlayer_Debug.ld" -o "WAVPlayer.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) WAVPlayer.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "WAVPlayer.axf"; # arm-none-eabi-objcopy -v -O binary "WAVPlayer.axf" "WAVPlayer.bin" ; # checksum -p LPC1114FD_102 -d "WAVPlayer.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
