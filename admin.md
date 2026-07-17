from django.contrib import admin

# Register your models here.
from django.contrib import admin
from .models import Room, Guest, Booking, Payment


@admin.register(Room)
class RoomAdmin(admin.ModelAdmin):
    list_display = ('room_number', 'room_type', 'price_per_night', 'is_available')
    list_filter = ('room_type', 'is_available')
    search_fields = ('room_number',)
    ordering = ('room_number',)


@admin.register(Guest)
class GuestAdmin(admin.ModelAdmin):
    list_display = ('first_name', 'last_name', 'email', 'phone')
    search_fields = ('first_name', 'last_name', 'email')
    ordering = ('last_name',)


@admin.register(Booking)
class BookingAdmin(admin.ModelAdmin):
    list_display = ('id', 'guest', 'room', 'check_in', 'check_out', 'status')
    list_filter = ('status', 'check_in', 'check_out')
    search_fields = ('guest__first_name', 'guest__last_name', 'room__room_number')
    ordering = ('-booking_date',)


@admin.register(Payment)
class PaymentAdmin(admin.ModelAdmin):
    list_display = ('booking', 'amount', 'payment_method', 'is_paid', 'payment_date')
    list_filter = ('payment_method', 'is_paid')
    search_fields = ('booking__guest__first_name', 'booking__guest__last_name')
    ordering = ('-payment_date',)

