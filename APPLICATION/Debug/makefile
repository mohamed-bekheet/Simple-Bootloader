################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
APPLICATION.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
APPLICATION.list \

OBJCOPY_HEX += \
APPLICATION.hex \

OBJCOPY_BIN += \
APPLICATION.bin \


# All Target
all: APPLICATION.elf secondary-outputs

# Tool invocations
APPLICATION.elf: $(OBJS) $(USER_OBJS) D:\1.Mohamed\Embedded\ARM_microController\projects\Test_BOOTLOADER2\APPLICATION\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "APPLICATION.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\1.Mohamed\Embedded\ARM_microController\projects\Test_BOOTLOADER2\APPLICATION\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="APPLICATION.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

APPLICATION.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "APPLICATION.list"
	@echo 'Finished building: $@'
	@echo ' '

APPLICATION.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "APPLICATION.hex"
	@echo 'Finished building: $@'
	@echo ' '

APPLICATION.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "APPLICATION.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
